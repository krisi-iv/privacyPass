# Privacy Pass and Privacy Pass Plus Tamarin Models

## Organization
1. **Models**
    - `privacyPass_D.spthy`: Tamarin model of the Privacy Pass protocol (PP) ([Davidson et al.](https://www.petsymposium.org/2018/files/papers/issue3/popets-2018-0026.pdf)). Includes correctness (*C*), one-more-token security (*SP1*), and single signing key (*SP3*) lemmas, verified under the default attack model *D*.
    - `privacyPass_S.spthy`: Tamarin model of the Privacy Pass protocol (PP) ([Davidson et al.](https://www.petsymposium.org/2018/files/papers/issue3/popets-2018-0026.pdf)). Includes correctness (*C*), one-more-token security (*SP1*), and single signing key (*SP3*) lemmas, verified under the stronger attack model *S*.
    - `privacyPass_plus.spthy`: Tamarin model of the Privacy Pass Plus protocol (PP+). Includes correctness (*C*), one-more-token security (*SP1*), and single signing key (*SP3*) lemma.
    - `SP2_Observational_Equivalence/pp_2_1.spthy`: Tamarin PP_2.1 model (simplification of PP), verifying the lemmas covering *A2.1*-*A2.4*.
    - `SP2_Observational_Equivalence/pp_2_2.spthy`: Tamarin PP_2.2 model (simplification of PP) for the unlinkability property (*SP2*) of the Privacy Pass protocol.
    - `SP2_Observational_Equivalence/pp_plus_2_1.spthy`: Tamarin PP+_2.1 model (simplification of PP+), verifying the lemmas covering *A2.1*-*A2.4*.
    - `SP2_Observational_Equivalence/pp_plus_2_2.spthy`: Tamarin PP+_2.2 model (simplification of PP+) for the unlinkability property (*SP2*) of the Privacy Pass Plus protocol.
2. **Oracles**
    - `privacy_pass.oracle`: The oracle used to speed up the verification of the single signing key property (*SP3*) of Privacy Pass models (PP: `privacyPass_D.spthy` and `privacyPass_S.spthy`).
    - `privacy_pass_plus.oracle`: The oracle used to speed up the verification of the correctness (*C*), one-more-token security (*SP1*), and single signing key (*SP3*) properties of the Privacy Pass Plus model (PP+: `privacyPass_plus.spthy`).
    - `SP2_Observational_Equivalence/pp_unlinkability.oracle`: The oracle used to speed up the verification of the observational equivalence (*SP2*) and the lemmas showing the adversary is unable to inject and/ or successfully modify tokens in the Privacy Pass simplification models (PP_2.1: `pp_2_1.spthy` and PP_2.2: `pp_2_2.spthy`).
    - `SP2_Observational_Equivalence/ pp_plus_unlinkability_redemption.oracle`: The oracle used to speed up the verification of the observational equivalence (*SP2*) and correctness (*C*) of the Privacy Pass Plus implification models (PP+_2.1: `pp_plus_2_1.spthy` and PP+_2.2: `pp_plus_2_2.spthy`).

3. **Manual Attack Trace**
    - `Manual_Proof/SP1_manual_proof_PP_model_S.spthy`: attack trace for the one-more-token security property for the Privacy Pass model (PP) under the strongr attack model(`privacyPass_S.spthy`).

## Flags 
The flag "MANUAL" is set for the `one_more_token_security` lemma in the `privacyPass_S.spthy` model to indicate that it has to be proven manually and the attack trace found is availabe in the `Manual_Proof/SP1_manual_proof_PP_model_S.spthy` file.


## Reproducing The Results

The models have been tested with version 1.10.0 of the [tamarin-prover](https://github.com/tamarin-prover/tamarin-prover) (installation and usage guide available in chapter 2 of the [manual](https://tamarin-prover.com/manual/master/book/002_installation.html)).

The beginning of each `.spthy` file contains instructions on how the model can be verified using Tamarin are included along with the results we obtained from the runs. 


The models using observational equivalence and verifying (*SP2*) can be found in the folder `SP2_Observational_Equivalence`.


