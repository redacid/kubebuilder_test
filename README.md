# kubebuilder_test

kubebuilder init --domain sr.ios.in.ua --plugins go/v4 --repo github.com/redacid/kubebuilder_test --project-name=redacid-test
kubebuilder create api --group prozorro --version v1alpha1 --kind MapRole
kubebuilder create api --group prozorro --version v1alpha1 --kind MapUser
kubebuilder create api --group prozorro --version v1alpha1 --kind MapAccount
