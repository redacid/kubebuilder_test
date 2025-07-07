# kubebuilder_test

kubebuilder init --domain sr.ios.in.ua --plugins go/v4 --repo github.com/redacid/kubebuilder_test --project-name=redacid-test
kubebuilder create api --group prozorro --version v1alpha1 --kind MapRole --namespaced false --controller --resource
kubebuilder create api --group prozorro --version v1alpha1 --kind MapUser --namespaced false --controller --resource

git tag 0.0.4 -m "Test 0.0.4"
git push origin 0.0.4

cd ./charts helm upgrade -i --namespace kube-system aws-auth aws-auth-operator
cd ./config/samples kubectl apply -f prozorro_v1alpha1_mapuser.yaml -n kube-system
cd ./config/samples kubectl apply -f prozorro.sr.ios.in.ua_maproles.yaml -n kube-system
