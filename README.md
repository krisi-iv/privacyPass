# Privacy Pass and Privacy Pass Plus Tamarin Models

## Organization
1. **Models**
    - `privacyPass.spthy`: Tamarin model of the Privacy Pass protocol ([Davidson et al.](https://www.petsymposium.org/2018/files/papers/issue3/popets-2018-0026.pdf)). Includes correctness, one-more-token security, and single signing key lemma.
    - `privacyPass_plus.spthy`: Tamarin model of the Privacy Pass Plus protocol. Includes correctness (*C*), one-more-token security (*SP1*), and single signing key (*SP4*) lemma.
    - `pp_unlinkability_issuance.spthy`: Tamarin model for the unlinkability property in the issuance phase (*SP2*) of the Privacy Pass and Privacy Pass Plus protocols.
    - `pp_unlinkability_redemption.spthy`: Tamarin model for the unlinkability property in the redemption phase (*SP3*) of the Privacy Pass protocol.
    - `pp_plus_unlinkability_redemption.spthy`: Tamarin model for the unlinkability property in the redemption phase (*SP3*) of the Privacy Pass Plus protocol.
2. **Oracles**
    - `privacy_pass_plus.oracle`: The oracle used to speed up the verification of the correctness and one-more-token security property of Privacy Pass Plus.
3. **Manual Attack Trace**
    - `SP1_manual_proof_PP_model.spthy`: attack trace for the one-more-token security property for the Privacy Pass model (`privacyPass.spthy`).

## Flags 
The flag "MANUAL" is set for the `one_more_token_security` lemma in the `privacyPass.spthy` model to indicate that it has to be proven manually and the attack trace found is available in the `SP1_manual_proof_PP_model.spthy` file.

## Reproducing The Results

The models have been tested with version 1.10.0 of the [tamarin-prover](https://github.com/tamarin-prover/tamarin-prover) (installation and usage guide available in chapter 2 of the [manual](https://tamarin-prover.com/manual/master/book/002_installation.html)).

The beginning of each `.spthy` file contains instructions on how the model can be verified using Tamarin, along with the results we obtained from the runs. 

