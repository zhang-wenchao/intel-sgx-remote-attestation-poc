Server:

```
[+] Init Enclave Successful 2!
Running as server...
new client from 127.0.0.1:43670
Entering ocall_sgx_init_quote
eg = [75, 12, 0, 0]
get_sigrl_from_intel fd = 6
GET /sgx/dev/attestation/v3/sigrl/00000c4b HTTP/1.1
HOST: api.trustedservices.intel.com
Ocp-Apim-Subscription-Key: 19f4076a892e4a9683288e8c824eeaf2
Connection: Close


write complete
read_to_end complete
HTTP/1.1 200 OK
Warning: 299 api.trustedservices.intel.com "The version of Attestation Service for Intel(R) Software Guard Extensions API you are using is scheduled to end of life on February 16th, 2023. For details on how to update to the latest version of the API, please refer to the IAS API spec [located here: https://www.intel.com/content/dam/develop/public/us/en/documents/sgx-attestation-api-spec.pdf]."
Content-Length: 0
Request-ID: e28164d8415d4beabdbe165d7131b57f
Date: Mon, 21 Nov 2022 20:46:11 GMT
Connection: close


parse_response_sigrl
parse result Ok(Complete(537))
parse responseResponse { version: Some(1), code: Some(200), reason: Some("OK"), headers: [Header { name: "Warning", value: "299 api.trustedservices.intel.com \"The version of Attestation Service for Intel(R) Software Guard Extensions API you are using is scheduled to end of life on February 16th, 2023. For details on how to update to the latest version of the API, please refer to the IAS API spec [located here: https://www.intel.com/content/dam/develop/public/us/en/documents/sgx-attestation-api-spec.pdf].\"" }, Header { name: "Content-Length", value: "0" }, Header { name: "Request-ID", value: "e28164d8415d4beabdbe165d7131b57f" }, Header { name: "Date", value: "Mon, 21 Nov 2022 20:46:11 GMT" }, Header { name: "Connection", value: "close" }] }
OK Operation Successful
Report creation => success [131, 215, 25, 231, 125, 234, 202, 20, 112, 246, 186, 246, 42, 77, 119, 67, 3, 200, 153, 219, 105, 2, 15, 156, 112, 238, 29, 252, 8, 199, 206, 158]
rand finished
Entering ocall_get_quote
quote size = 1116
sgx_calc_quote_size returned SGX_SUCCESS.
rsgx_verify_report passed!
qe_report check passed
rhs hash = C65D84B3D0895C34777D5A31E26D6194DA3DD04E06CA6D0BBCDCB41F31A32C0E
report hs= C65D84B3D0895C34777D5A31E26D6194DA3DD04E06CA6D0BBCDCB41F31A32C0E
get_report_from_intel fd = 6
POST /sgx/dev/attestation/v3/report HTTP/1.1
HOST: api.trustedservices.intel.com
Ocp-Apim-Subscription-Key:19f4076a892e4a9683288e8c824eeaf2
Content-Length:1512
Content-Type: application/json
Connection: close

{"isvEnclaveQuote":"AgAAAEsMAAANAA0AAAAAAC9GSPlu9PnNQz0bjbjDPjjtQL9vqwxxt49o3Q6etxHnExMCB/+ABgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABwAAAAAAAAAHAAAAAAAAACulRC4tliigpbA4CYa+807lIlyroA5z/qKUszbsQ1LrAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACD1xnnferKFHD2uvYqTXdDA8iZ22kCD5xw7h38CMfOngAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAyHzozYCFOm7ZPBgvF2RX4WqPTe5OW6+swDprOh4eqNF3ur1VoKg1lhJumABBJr7c2Lbv8xycckZl6ye6XNHFDqAIAAFvxQagjt9ZH/6urJ6hxj7myFSUHbrfElFYt4DFBFSuahuFGaWEiEHMCgWVs9/ydnDczcaB2k7lOuv+02op6uEHIFIQvlyVDJ4O/ClgWKUXYDCZQ3AqFe36SM15vZ2a4OdDv6UU2VKcyG/1xWnIuWiq5MfNBCLyE/vkdbP+mpMta2mDWJBrqygU884wOkbbXxVGOeVhwsF+JDi1p3huLNP9K9RTWLLRIZg+o/dI2Z+jyUlcjGNqw7++5EHg5rf5+DYo7FvT6ddFcFQ5kbEkSPQW3Cn8vWU/sbabWC0u+w3l3QFly8ZnaoH8FyhWIqKrhMtzU1Ccu/F8UMHOLlwSjEmoECesXyOYehyWouFX52ANo88zNT4oypKLnarsCbulLUqrMi47uumorbeXuQmgBAAAwlyC4mHVykEcQ80V9AzaU1jmnjPPmUFp3CwbOpOuJa7m96ih56+Hwjkn2oH+cOOkhcPQVyWgwLqQ18w5oXv3su171OmDudSsWlo4rJhadicarpyw5zcGb588YJE3sfkE9xXcreChGMJ5ycjEbf4xQk0bVCKdaBnxHkHBgx9i4aswaej72ceJNG9kAWqXYgecFdpKpggUx7SAj/Go4lnr0NhbVojBX7sTCpW4CFc3O/JWIAMBEwfJtBoTz208qv0K3TVzc2jCopEkIanrqziFKNvcBATkf6Ok+8jES1z1vcqCYmqLq6zw1d8K+CNZ9qjFa6EnyqRk3X5QxzudaOFNWhQj8cGRn/s/DIu9c4+YCBL2v4uLgPTyvKT98D99g2idH7Tlrvf5tdROk+YNHX/JeniqOLg/J92dzFgTOggZx/NSeSRQ79zDxtMcztIddfK26fxxaRuXWq7+wG3k3WNar0bf+fBWcKLjvMLXa/4y0pJ5VUvumU37+"}

write complete
read_to_end complete
resp_string = HTTP/1.1 200 OK
Warning: 299 api.trustedservices.intel.com "The version of Attestation Service for Intel(R) Software Guard Extensions API you are using is scheduled to end of life on February 16th, 2023. For details on how to update to the latest version of the API, please refer to the IAS API spec [located here: https://www.intel.com/content/dam/develop/public/us/en/documents/sgx-attestation-api-spec.pdf]."
Content-Length: 730
Content-Type: application/json
Request-ID: 67b94220e4df4118ae101e0ccabfa50f
X-IASReport-Signature: NbaBL+DB8+GwWV43VnrwV6+Hzp9cmwQyURcW0OBeZ6gD7B3z3dsINIjKZmRClnweYK7lsBFKsUEa9zM/9lq2o7MvNrmR2XUqdI3Jp2PsFaMfTNVy2XTN/SSNRGFd0ycNpQVEcnv8UiPBH0tH9/BhTdSrp6kMOaTAf9nVh3ZCYhX5i4Ut2hAPN1La5KQVeyTYQcz9HSxUcLKfBk5qpNxO81nGAZCqpBokD1GurIJgJjJNUwZKTJvREWHYn/egS5G56YkTqK0MXuzHBGk3djMkr6SRAMERL+Kz30DygnzA8xSdX4WFLdVEnp+XwgL5SNzeoAuLFuTVJUMR6Z6IHsstQA==
X-IASReport-Signing-Certificate: -----BEGIN%20CERTIFICATE-----%0AMIIEoTCCAwmgAwIBAgIJANEHdl0yo7CWMA0GCSqGSIb3DQEBCwUAMH4xCzAJBgNV%0ABAYTAlVTMQswCQYDVQQIDAJDQTEUMBIGA1UEBwwLU2FudGEgQ2xhcmExGjAYBgNV%0ABAoMEUludGVsIENvcnBvcmF0aW9uMTAwLgYDVQQDDCdJbnRlbCBTR1ggQXR0ZXN0%0AYXRpb24gUmVwb3J0IFNpZ25pbmcgQ0EwHhcNMTYxMTIyMDkzNjU4WhcNMjYxMTIw%0AMDkzNjU4WjB7MQswCQYDVQQGEwJVUzELMAkGA1UECAwCQ0ExFDASBgNVBAcMC1Nh%0AbnRhIENsYXJhMRowGAYDVQQKDBFJbnRlbCBDb3Jwb3JhdGlvbjEtMCsGA1UEAwwk%0ASW50ZWwgU0dYIEF0dGVzdGF0aW9uIFJlcG9ydCBTaWduaW5nMIIBIjANBgkqhkiG%0A9w0BAQEFAAOCAQ8AMIIBCgKCAQEAqXot4OZuphR8nudFrAFiaGxxkgma%2FEs%2FBA%2Bt%0AbeCTUR106AL1ENcWA4FX3K%2BE9BBL0%2F7X5rj5nIgX%2FR%2F1ubhkKWw9gfqPG3KeAtId%0Acv%2FuTO1yXv50vqaPvE1CRChvzdS%2FZEBqQ5oVvLTPZ3VEicQjlytKgN9cLnxbwtuv%0ALUK7eyRPfJW%2FksddOzP8VBBniolYnRCD2jrMRZ8nBM2ZWYwnXnwYeOAHV%2BW9tOhA%0AImwRwKF%2F95yAsVwd21ryHMJBcGH70qLagZ7Ttyt%2B%2BqO%2F6%2BKAXJuKwZqjRlEtSEz8%0AgZQeFfVYgcwSfo96oSMAzVr7V0L6HSDLRnpb6xxmbPdqNol4tQIDAQABo4GkMIGh%0AMB8GA1UdIwQYMBaAFHhDe3amfrzQr35CN%2Bs1fDuHAVE8MA4GA1UdDwEB%2FwQEAwIG%0AwDAMBgNVHRMBAf8EAjAAMGAGA1UdHwRZMFcwVaBToFGGT2h0dHA6Ly90cnVzdGVk%0Ac2VydmljZXMuaW50ZWwuY29tL2NvbnRlbnQvQ1JML1NHWC9BdHRlc3RhdGlvblJl%0AcG9ydFNpZ25pbmdDQS5jcmwwDQYJKoZIhvcNAQELBQADggGBAGcIthtcK9IVRz4r%0ARq%2BZKE%2B7k50%2FOxUsmW8aavOzKb0iCx07YQ9rzi5nU73tME2yGRLzhSViFs%2FLpFa9%0AlpQL6JL1aQwmDR74TxYGBAIi5f4I5TJoCCEqRHz91kpG6Uvyn2tLmnIdJbPE4vYv%0AWLrtXXfFBSSPD4Afn7%2B3%2FXUggAlc7oCTizOfbbtOFlYA4g5KcYgS1J2ZAeMQqbUd%0AZseZCcaZZZn65tdqee8UXZlDvx0%2BNdO0LR%2B5pFy%2BjuM0wWbu59MvzcmTXbjsi7HY%0A6zd53Yq5K244fwFHRQ8eOB0IWB%2B4PfM7FeAApZvlfqlKOlLcZL2uyVmzRkyR5yW7%0A2uo9mehX44CiPJ2fse9Y6eQtcfEhMPkmHXI01sN%2BKwPbpA39%2BxOsStjhP9N1Y1a2%0AtQAVo%2ByVgLgV2Hws73Fc0o3wC78qPEA%2Bv2aRs%2FBe3ZFDgDyghc%2F1fgU%2B7C%2BP6kbq%0Ad4poyb6IW8KCJbxfMJvkordNOgOUUxndPHEi%2Ftb%2FU7uLjLOgPA%3D%3D%0A-----END%20CERTIFICATE-----%0A-----BEGIN%20CERTIFICATE-----%0AMIIFSzCCA7OgAwIBAgIJANEHdl0yo7CUMA0GCSqGSIb3DQEBCwUAMH4xCzAJBgNV%0ABAYTAlVTMQswCQYDVQQIDAJDQTEUMBIGA1UEBwwLU2FudGEgQ2xhcmExGjAYBgNV%0ABAoMEUludGVsIENvcnBvcmF0aW9uMTAwLgYDVQQDDCdJbnRlbCBTR1ggQXR0ZXN0%0AYXRpb24gUmVwb3J0IFNpZ25pbmcgQ0EwIBcNMTYxMTE0MTUzNzMxWhgPMjA0OTEy%0AMzEyMzU5NTlaMH4xCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJDQTEUMBIGA1UEBwwL%0AU2FudGEgQ2xhcmExGjAYBgNVBAoMEUludGVsIENvcnBvcmF0aW9uMTAwLgYDVQQD%0ADCdJbnRlbCBTR1ggQXR0ZXN0YXRpb24gUmVwb3J0IFNpZ25pbmcgQ0EwggGiMA0G%0ACSqGSIb3DQEBAQUAA4IBjwAwggGKAoIBgQCfPGR%2BtXc8u1EtJzLA10Feu1Wg%2Bp7e%0ALmSRmeaCHbkQ1TF3Nwl3RmpqXkeGzNLd69QUnWovYyVSndEMyYc3sHecGgfinEeh%0ArgBJSEdsSJ9FpaFdesjsxqzGRa20PYdnnfWcCTvFoulpbFR4VBuXnnVLVzkUvlXT%0AL%2FTAnd8nIZk0zZkFJ7P5LtePvykkar7LcSQO85wtcQe0R1Raf%2FsQ6wYKaKmFgCGe%0ANpEJUmg4ktal4qgIAxk%2BQHUxQE42sxViN5mqglB0QJdUot%2Fo9a%2FV%2FmMeH8KvOAiQ%0AbyinkNndn%2BBgk5sSV5DFgF0DffVqmVMblt5p3jPtImzBIH0QQrXJq39AT8cRwP5H%0AafuVeLHcDsRp6hol4P%2BZFIhu8mmbI1u0hH3W%2F0C2BuYXB5PC%2B5izFFh%2FnP0lc2Lf%0A6rELO9LZdnOhpL1ExFOq9H%2FB8tPQ84T3Sgb4nAifDabNt%2Fzu6MmCGo5U8lwEFtGM%0ARoOaX4AS%2B909x00lYnmtwsDVWv9vBiJCXRsCAwEAAaOByTCBxjBgBgNVHR8EWTBX%0AMFWgU6BRhk9odHRwOi8vdHJ1c3RlZHNlcnZpY2VzLmludGVsLmNvbS9jb250ZW50%0AL0NSTC9TR1gvQXR0ZXN0YXRpb25SZXBvcnRTaWduaW5nQ0EuY3JsMB0GA1UdDgQW%0ABBR4Q3t2pn680K9%2BQjfrNXw7hwFRPDAfBgNVHSMEGDAWgBR4Q3t2pn680K9%2BQjfr%0ANXw7hwFRPDAOBgNVHQ8BAf8EBAMCAQYwEgYDVR0TAQH%2FBAgwBgEB%2FwIBADANBgkq%0AhkiG9w0BAQsFAAOCAYEAeF8tYMXICvQqeXYQITkV2oLJsp6J4JAqJabHWxYJHGir%0AIEqucRiJSSx%2BHjIJEUVaj8E0QjEud6Y5lNmXlcjqRXaCPOqK0eGRz6hi%2BripMtPZ%0AsFNaBwLQVV905SDjAzDzNIDnrcnXyB4gcDFCvwDFKKgLRjOB%2FWAqgscDUoGq5ZVi%0AzLUzTqiQPmULAQaB9c6Oti6snEFJiCQ67JLyW%2FE83%2FfrzCmO5Ru6WjU4tmsmy8Ra%0AUd4APK0wZTGtfPXU7w%2BIBdG5Ez0kE1qzxGQaL4gINJ1zMyleDnbuS8UicjJijvqA%0A152Sq049ESDz%2B1rRGc2NVEqh1KaGXmtXvqxXcTB%2BLjy5Bw2ke0v8iGngFBPqCTVB%0A3op5KBG3RjbF6RRSzwzuWfL7QErNC8WEy5yDVARzTA5%2BxmBc388v9Dm21HGfcC8O%0ADD%2BgT9sSpssq0ascmvH49MOgjt1yoysLtdCtJW%2F9FZpoOypaHx0R%2BmJTLwPXVMrv%0ADaVzWh5aiEx%2BidkSGMnX%0A-----END%20CERTIFICATE-----%0A
Date: Mon, 21 Nov 2022 20:46:12 GMT
Connection: close

{"id":"39764797212119215723162443106314571679","timestamp":"2022-11-21T20:46:12.280427","version":3,"isvEnclaveQuoteStatus":"OK","isvEnclaveQuoteBody":"AgAAAEsMAAANAA0AAAAAAC9GSPlu9PnNQz0bjbjDPjjtQL9vqwxxt49o3Q6etxHnExMCB/+ABgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABwAAAAAAAAAHAAAAAAAAACulRC4tliigpbA4CYa+807lIlyroA5z/qKUszbsQ1LrAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACD1xnnferKFHD2uvYqTXdDA8iZ22kCD5xw7h38CMfOngAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAyHzozYCFOm7ZPBgvF2RX4WqPTe5OW6+swDprOh4eqNF3ur1VoKg1lhJumABBJr7c2Lbv8xycckZl6ye6XNHFD"}
parse_response_attn_report
parse result Ok(Complete(4807))
OK Operation Successful
content length = 730
Attestation report: {"id":"39764797212119215723162443106314571679","timestamp":"2022-11-21T20:46:12.280427","version":3,"isvEnclaveQuoteStatus":"OK","isvEnclaveQuoteBody":"AgAAAEsMAAANAA0AAAAAAC9GSPlu9PnNQz0bjbjDPjjtQL9vqwxxt49o3Q6etxHnExMCB/+ABgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABwAAAAAAAAAHAAAAAAAAACulRC4tliigpbA4CYa+807lIlyroA5z/qKUszbsQ1LrAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACD1xnnferKFHD2uvYqTXdDA8iZ22kCD5xw7h38CMfOngAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAyHzozYCFOm7ZPBgvF2RX4WqPTe5OW6+swDprOh4eqNF3ur1VoKg1lhJumABBJr7c2Lbv8xycckZl6ye6XNHFD"}
client cert: [Certificate(b"0\x82\x0b\x950\x82\x0b:\xa0\x03\x02\x01\x02\x02\x01\x010\n\x06\x08*\x86H\xce=\x04\x03\x020\x121\x100\x0e\x06\x03U\x04\x03\x0c\x07MesaTEE0\x1e\x17\r221121204612Z\x17\r230219204612Z0\x121\x100\x0e\x06\x03U\x04\x03\x0c\x07MesaTEE0Y0\x13\x06\x07*\x86H\xce=\x02\x01\x06\x08*\x86H\xce=\x03\x01\x07\x03B\0\x04\xed'\xb7\xa2\0VX\xd1\x7f\x0e\xb2\x1b\x12o\x883\xc4y\x11\xee2\xbeO\xa6\"\x1b\xc4\xf7o\0\xf4d\x1c\xeb3\xce\x195\xb7\x1e\x08wt\xab=\xa9\xa3\x8a\xc7\xd6\xe1\xeb\x1eF\x14\xa7{!\xdf\xd6\xc0\xb8\x92\x8b\xa3\x82\n\x7f0\x82\n{0\x82\nw\x06\t`\x86H\x01\x86\xf8B\x01\r\x04\x82\nh{\"id\":\"30269556922087116282920178870493890659\",\"timestamp\":\"2022-11-21T20:46:12.479104\",\"version\":3,\"isvEnclaveQuoteStatus\":\"OK\",\"isvEnclaveQuoteBody\":\"AgAAAEsMAAANAA0AAAAAAC9GSPlu9PnNQz0bjbjDPjhUxSAKFxTqVEPKCLDUH32aExMCB/+ABgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABwAAAAAAAAAHAAAAAAAAACulRC4tliigpbA4CYa+807lIlyroA5z/qKUszbsQ1LrAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACD1xnnferKFHD2uvYqTXdDA8iZ22kCD5xw7h38CMfOngAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAADtJ7eiAFZY0X8OshsSb4gzxHkR7jK+T6YiG8T3bwD0ZBzrM84ZNbceCHd0qz2po4rH1uHrHkYUp3sh39bAuJKL\"}|mKh/wgL6wBuRXnWqxzwniO1Mz9ynJ7bNewVTekeuuZTsZL1dlW0+C4NovWT/egTxqw2IVFgLpnkG2oYJSpL9F7+Nx23LDREeaZM/sY6o5WA0ypbDWrRgZBZqQXX4Q6FJDbVbO6TKonTz6NudJn+Br9yogsT8iHCF/KMasbqcaak7IXekKgwrVXuhVMXTdQMIGFiCrq2mKxQ1nnf4wWAusTbYihTXcXla0Of/oLtVdfz+xsyThI4NR+FIjzs3l3ql+8wovCirDrYjivIPXbYcD+fHOsBjMXn/BhMP4HqIJoOJVtCBnL22lRdIbtod0ggLmiTQ62p+GQQ9Od0Z3T998Q==|MIIEoTCCAwmgAwIBAgIJANEHdl0yo7CWMA0GCSqGSIb3DQEBCwUAMH4xCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJDQTEUMBIGA1UEBwwLU2FudGEgQ2xhcmExGjAYBgNVBAoMEUludGVsIENvcnBvcmF0aW9uMTAwLgYDVQQDDCdJbnRlbCBTR1ggQXR0ZXN0YXRpb24gUmVwb3J0IFNpZ25pbmcgQ0EwHhcNMTYxMTIyMDkzNjU4WhcNMjYxMTIwMDkzNjU4WjB7MQswCQYDVQQGEwJVUzELMAkGA1UECAwCQ0ExFDASBgNVBAcMC1NhbnRhIENsYXJhMRowGAYDVQQKDBFJbnRlbCBDb3Jwb3JhdGlvbjEtMCsGA1UEAwwkSW50ZWwgU0dYIEF0dGVzdGF0aW9uIFJlcG9ydCBTaWduaW5nMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAqXot4OZuphR8nudFrAFiaGxxkgma/Es/BA+tbeCTUR106AL1ENcWA4FX3K+E9BBL0/7X5rj5nIgX/R/1ubhkKWw9gfqPG3KeAtIdcv/uTO1yXv50vqaPvE1CRChvzdS/ZEBqQ5oVvLTPZ3VEicQjlytKgN9cLnxbwtuvLUK7eyRPfJW/ksddOzP8VBBniolYnRCD2jrMRZ8nBM2ZWYwnXnwYeOAHV+W9tOhAImwRwKF/95yAsVwd21ryHMJBcGH70qLagZ7Ttyt++qO/6+KAXJuKwZqjRlEtSEz8gZQeFfVYgcwSfo96oSMAzVr7V0L6HSDLRnpb6xxmbPdqNol4tQIDAQABo4GkMIGhMB8GA1UdIwQYMBaAFHhDe3amfrzQr35CN+s1fDuHAVE8MA4GA1UdDwEB/wQEAwIGwDAMBgNVHRMBAf8EAjAAMGAGA1UdHwRZMFcwVaBToFGGT2h0dHA6Ly90cnVzdGVkc2VydmljZXMuaW50ZWwuY29tL2NvbnRlbnQvQ1JML1NHWC9BdHRlc3RhdGlvblJlcG9ydFNpZ25pbmdDQS5jcmwwDQYJKoZIhvcNAQELBQADggGBAGcIthtcK9IVRz4rRq+ZKE+7k50/OxUsmW8aavOzKb0iCx07YQ9rzi5nU73tME2yGRLzhSViFs/LpFa9lpQL6JL1aQwmDR74TxYGBAIi5f4I5TJoCCEqRHz91kpG6Uvyn2tLmnIdJbPE4vYvWLrtXXfFBSSPD4Afn7+3/XUggAlc7oCTizOfbbtOFlYA4g5KcYgS1J2ZAeMQqbUdZseZCcaZZZn65tdqee8UXZlDvx0+NdO0LR+5pFy+juM0wWbu59MvzcmTXbjsi7HY6zd53Yq5K244fwFHRQ8eOB0IWB+4PfM7FeAApZvlfqlKOlLcZL2uyVmzRkyR5yW72uo9mehX44CiPJ2fse9Y6eQtcfEhMPkmHXI01sN+KwPbpA39+xOsStjhP9N1Y1a2tQAVo+yVgLgV2Hws73Fc0o3wC78qPEA+v2aRs/Be3ZFDgDyghc/1fgU+7C+P6kbqd4poyb6IW8KCJbxfMJvkordNOgOUUxndPHEi/tb/U7uLjLOgPA==0\n\x06\x08*\x86H\xce=\x04\x03\x02\x03I\00F\x02!\0\xe7<\xce\xf2\xda\xfd\x98\xdc\xa8\xf9\x8a\xc9\x13.\xee\x9cX:\x8d=<\xcf\x9b\x94G\xeevP\xb8\xb3\xab\x95\x02!\0\x8a\xdf\x1d\t\xa8\xd1!\xaa\xf5\xb2\xc7\xf85\xdc.\x8a\x93F\x81\xdf,\xfb-J\xd5\x92\xf1\x16A\xa3\x12\x85")]
Cert is good
Signature good
Time diff = 0
isvEnclaveQuoteStatus = OK
Quote = [2, 0, 0, 0, 75, 12, 0, 0, 13, 0, 13, 0, 0, 0, 0, 0, 47, 70, 72, 249, 110, 244, 249, 205, 67, 61, 27, 141, 184, 195, 62, 56, 84, 197, 32, 10, 23, 20, 234, 84, 67, 202, 8, 176, 212, 31, 125, 154, 19, 19, 2, 7, 255, 128, 6, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 7, 0, 0, 0, 0, 0, 0, 0, 7, 0, 0, 0, 0, 0, 0, 0, 43, 165, 68, 46, 45, 150, 40, 160, 165, 176, 56, 9, 134, 190, 243, 78, 229, 34, 92, 171, 160, 14, 115, 254, 162, 148, 179, 54, 236, 67, 82, 235, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 131, 215, 25, 231, 125, 234, 202, 20, 112, 246, 186, 246, 42, 77, 119, 67, 3, 200, 153, 219, 105, 2, 15, 156, 112, 238, 29, 252, 8, 199, 206, 158, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 237, 39, 183, 162, 0, 86, 88, 209, 127, 14, 178, 27, 18, 111, 136, 51, 196, 121, 17, 238, 50, 190, 79, 166, 34, 27, 196, 247, 111, 0, 244, 100, 28, 235, 51, 206, 25, 53, 183, 30, 8, 119, 116, 171, 61, 169, 163, 138, 199, 214, 225, 235, 30, 70, 20, 167, 123, 33, 223, 214, 192, 184, 146, 139]
sgx quote version = 2
sgx quote signature type = 0
sgx quote report_data = ed27b7a2005658d17f0eb21b126f8833c47911ee32be4fa6221bc4f76f00f4641ceb33ce1935b71e087774ab3da9a38ac7d6e1eb1e4614a77b21dfd6c0b8928b
sgx quote mr_enclave = 2ba5442e2d9628a0a5b0380986bef34ee5225caba00e73fea294b336ec4352eb
sgx quote mr_signer = 83d719e77deaca1470f6baf62a4d774303c899db69020f9c70ee1dfc08c7ce9e
Anticipated public key = ed27b7a2005658d17f0eb21b126f8833c47911ee32be4fa6221bc4f76f00f4641ceb33ce1935b71e087774ab3da9a38ac7d6e1eb1e4614a77b21dfd6c0b8928b
Mutual RA done!
Client said: hello
ECALL success!
[+] Done!
```

Client:


```

[+] Init Enclave Successful 2!
Running as client...
Entering ocall_sgx_init_quote
eg = [75, 12, 0, 0]
get_sigrl_from_intel fd = 5
GET /sgx/dev/attestation/v3/sigrl/00000c4b HTTP/1.1
HOST: api.trustedservices.intel.com
Ocp-Apim-Subscription-Key: 19f4076a892e4a9683288e8c824eeaf2
Connection: Close


write complete
read_to_end complete
HTTP/1.1 200 OK
Warning: 299 api.trustedservices.intel.com "The version of Attestation Service for Intel(R) Software Guard Extensions API you are using is scheduled to end of life on February 16th, 2023. For details on how to update to the latest version of the API, please refer to the IAS API spec [located here: https://www.intel.com/content/dam/develop/public/us/en/documents/sgx-attestation-api-spec.pdf]."
Content-Length: 0
Request-ID: 53ff5314c2984a80b95f9af9e005a844
Date: Mon, 21 Nov 2022 20:46:11 GMT
Connection: close


parse_response_sigrl
parse result Ok(Complete(537))
parse responseResponse { version: Some(1), code: Some(200), reason: Some("OK"), headers: [Header { name: "Warning", value: "299 api.trustedservices.intel.com \"The version of Attestation Service for Intel(R) Software Guard Extensions API you are using is scheduled to end of life on February 16th, 2023. For details on how to update to the latest version of the API, please refer to the IAS API spec [located here: https://www.intel.com/content/dam/develop/public/us/en/documents/sgx-attestation-api-spec.pdf].\"" }, Header { name: "Content-Length", value: "0" }, Header { name: "Request-ID", value: "53ff5314c2984a80b95f9af9e005a844" }, Header { name: "Date", value: "Mon, 21 Nov 2022 20:46:11 GMT" }, Header { name: "Connection", value: "close" }] }
OK Operation Successful
Report creation => success [131, 215, 25, 231, 125, 234, 202, 20, 112, 246, 186, 246, 42, 77, 119, 67, 3, 200, 153, 219, 105, 2, 15, 156, 112, 238, 29, 252, 8, 199, 206, 158]
rand finished
Entering ocall_get_quote
quote size = 1116
sgx_calc_quote_size returned SGX_SUCCESS.
rsgx_verify_report passed!
qe_report check passed
rhs hash = 8852CFD245798ACA440805D005C70B6ECAF8BD999967680B5F7A820941639A66
report hs= 8852CFD245798ACA440805D005C70B6ECAF8BD999967680B5F7A820941639A66
get_report_from_intel fd = 5
POST /sgx/dev/attestation/v3/report HTTP/1.1
HOST: api.trustedservices.intel.com
Ocp-Apim-Subscription-Key:19f4076a892e4a9683288e8c824eeaf2
Content-Length:1512
Content-Type: application/json
Connection: close

{"isvEnclaveQuote":"AgAAAEsMAAANAA0AAAAAAC9GSPlu9PnNQz0bjbjDPjhUxSAKFxTqVEPKCLDUH32aExMCB/+ABgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABwAAAAAAAAAHAAAAAAAAACulRC4tliigpbA4CYa+807lIlyroA5z/qKUszbsQ1LrAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACD1xnnferKFHD2uvYqTXdDA8iZ22kCD5xw7h38CMfOngAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAADtJ7eiAFZY0X8OshsSb4gzxHkR7jK+T6YiG8T3bwD0ZBzrM84ZNbceCHd0qz2po4rH1uHrHkYUp3sh39bAuJKLqAIAAIwADkhECbceVhJ1OYxko9nVN1AKE9yotOjGNE7l3Z4tHYZmF7myq1AqqkAwXBH2oFglEDaRQffhMZ5poJXtBltqHJQlI30NRD8aWEeKgndKLI5TFseLanH19XGSlvP5Dn+zW0+rPlu/n8TPqhe8SgutmGfRBENUh0dXAy3CHjpfvyHMZZHdk4xN02L0myYF7lEU6PzPbf1tmYfQEyp0vKdPHIS1W4nQqzvPxToLdNp6H8Umd4TCpHAHx+m3vJn+61gYrpVa5Sg5oGWqOAMww+Ji99BCTBEAbOoxhBBxi7lgv9wfQZR3Z5tedMDCp6derqhylXtfPaLPwqIg1IvdqlSbbPSMcJ13jK1TVBhIDQl+e+VntyTNNDjSDvwbIVk3ST9XUSVhyRZaYfJE1WgBAAAClDTbdRbJbjk9UFby2pfd5KCmFHpZZrDBfmTzFMhK1tufWG5j5lCEOJXVbu/GW/D2eyQmyY9hLURBdu++onbkQ3I5lYD3LAh5VvbNfD+XCbvRJ7dbqH5GqeUYRRuxDDgl6Z4GGFIBZ+rUt8AlS2+AMCWdHwPvqUrrUJU2/i87cgfS/SJhYBxyh3g/1CAzjw0ds+Iq+kkGcGye4BFxClb84j5+S/PPRsscIOqj4AClg6V1jMmKSnnF+679aVJY7wixwXmS5FbJPECpM9kd9ncL+1tBNyZDeZUH0zztutp09nCUluEuj1vVd7cQn2HYQKAwf2IBVemknlWdz7BEiD9eiMWy2viceX2BGaXILIQwopAYcMLIQG7MQPBPBb1JvhguxeCL84rhpBd1SgfbiVlqF/VxrhOvDJKx59LcWlTChVGE/9MWka99rIyQhm/VtLMjv3EvkMLMvxsqQxAVap2rupuhSPHrBdQsc+AHR+exXekU3evey3tK"}

write complete
read_to_end complete
resp_string = HTTP/1.1 200 OK
Warning: 299 api.trustedservices.intel.com "The version of Attestation Service for Intel(R) Software Guard Extensions API you are using is scheduled to end of life on February 16th, 2023. For details on how to update to the latest version of the API, please refer to the IAS API spec [located here: https://www.intel.com/content/dam/develop/public/us/en/documents/sgx-attestation-api-spec.pdf]."
Content-Length: 730
Content-Type: application/json
Request-ID: 912cbaacbe9849508d2c70e8274d7630
X-IASReport-Signature: mKh/wgL6wBuRXnWqxzwniO1Mz9ynJ7bNewVTekeuuZTsZL1dlW0+C4NovWT/egTxqw2IVFgLpnkG2oYJSpL9F7+Nx23LDREeaZM/sY6o5WA0ypbDWrRgZBZqQXX4Q6FJDbVbO6TKonTz6NudJn+Br9yogsT8iHCF/KMasbqcaak7IXekKgwrVXuhVMXTdQMIGFiCrq2mKxQ1nnf4wWAusTbYihTXcXla0Of/oLtVdfz+xsyThI4NR+FIjzs3l3ql+8wovCirDrYjivIPXbYcD+fHOsBjMXn/BhMP4HqIJoOJVtCBnL22lRdIbtod0ggLmiTQ62p+GQQ9Od0Z3T998Q==
X-IASReport-Signing-Certificate: -----BEGIN%20CERTIFICATE-----%0AMIIEoTCCAwmgAwIBAgIJANEHdl0yo7CWMA0GCSqGSIb3DQEBCwUAMH4xCzAJBgNV%0ABAYTAlVTMQswCQYDVQQIDAJDQTEUMBIGA1UEBwwLU2FudGEgQ2xhcmExGjAYBgNV%0ABAoMEUludGVsIENvcnBvcmF0aW9uMTAwLgYDVQQDDCdJbnRlbCBTR1ggQXR0ZXN0%0AYXRpb24gUmVwb3J0IFNpZ25pbmcgQ0EwHhcNMTYxMTIyMDkzNjU4WhcNMjYxMTIw%0AMDkzNjU4WjB7MQswCQYDVQQGEwJVUzELMAkGA1UECAwCQ0ExFDASBgNVBAcMC1Nh%0AbnRhIENsYXJhMRowGAYDVQQKDBFJbnRlbCBDb3Jwb3JhdGlvbjEtMCsGA1UEAwwk%0ASW50ZWwgU0dYIEF0dGVzdGF0aW9uIFJlcG9ydCBTaWduaW5nMIIBIjANBgkqhkiG%0A9w0BAQEFAAOCAQ8AMIIBCgKCAQEAqXot4OZuphR8nudFrAFiaGxxkgma%2FEs%2FBA%2Bt%0AbeCTUR106AL1ENcWA4FX3K%2BE9BBL0%2F7X5rj5nIgX%2FR%2F1ubhkKWw9gfqPG3KeAtId%0Acv%2FuTO1yXv50vqaPvE1CRChvzdS%2FZEBqQ5oVvLTPZ3VEicQjlytKgN9cLnxbwtuv%0ALUK7eyRPfJW%2FksddOzP8VBBniolYnRCD2jrMRZ8nBM2ZWYwnXnwYeOAHV%2BW9tOhA%0AImwRwKF%2F95yAsVwd21ryHMJBcGH70qLagZ7Ttyt%2B%2BqO%2F6%2BKAXJuKwZqjRlEtSEz8%0AgZQeFfVYgcwSfo96oSMAzVr7V0L6HSDLRnpb6xxmbPdqNol4tQIDAQABo4GkMIGh%0AMB8GA1UdIwQYMBaAFHhDe3amfrzQr35CN%2Bs1fDuHAVE8MA4GA1UdDwEB%2FwQEAwIG%0AwDAMBgNVHRMBAf8EAjAAMGAGA1UdHwRZMFcwVaBToFGGT2h0dHA6Ly90cnVzdGVk%0Ac2VydmljZXMuaW50ZWwuY29tL2NvbnRlbnQvQ1JML1NHWC9BdHRlc3RhdGlvblJl%0AcG9ydFNpZ25pbmdDQS5jcmwwDQYJKoZIhvcNAQELBQADggGBAGcIthtcK9IVRz4r%0ARq%2BZKE%2B7k50%2FOxUsmW8aavOzKb0iCx07YQ9rzi5nU73tME2yGRLzhSViFs%2FLpFa9%0AlpQL6JL1aQwmDR74TxYGBAIi5f4I5TJoCCEqRHz91kpG6Uvyn2tLmnIdJbPE4vYv%0AWLrtXXfFBSSPD4Afn7%2B3%2FXUggAlc7oCTizOfbbtOFlYA4g5KcYgS1J2ZAeMQqbUd%0AZseZCcaZZZn65tdqee8UXZlDvx0%2BNdO0LR%2B5pFy%2BjuM0wWbu59MvzcmTXbjsi7HY%0A6zd53Yq5K244fwFHRQ8eOB0IWB%2B4PfM7FeAApZvlfqlKOlLcZL2uyVmzRkyR5yW7%0A2uo9mehX44CiPJ2fse9Y6eQtcfEhMPkmHXI01sN%2BKwPbpA39%2BxOsStjhP9N1Y1a2%0AtQAVo%2ByVgLgV2Hws73Fc0o3wC78qPEA%2Bv2aRs%2FBe3ZFDgDyghc%2F1fgU%2B7C%2BP6kbq%0Ad4poyb6IW8KCJbxfMJvkordNOgOUUxndPHEi%2Ftb%2FU7uLjLOgPA%3D%3D%0A-----END%20CERTIFICATE-----%0A-----BEGIN%20CERTIFICATE-----%0AMIIFSzCCA7OgAwIBAgIJANEHdl0yo7CUMA0GCSqGSIb3DQEBCwUAMH4xCzAJBgNV%0ABAYTAlVTMQswCQYDVQQIDAJDQTEUMBIGA1UEBwwLU2FudGEgQ2xhcmExGjAYBgNV%0ABAoMEUludGVsIENvcnBvcmF0aW9uMTAwLgYDVQQDDCdJbnRlbCBTR1ggQXR0ZXN0%0AYXRpb24gUmVwb3J0IFNpZ25pbmcgQ0EwIBcNMTYxMTE0MTUzNzMxWhgPMjA0OTEy%0AMzEyMzU5NTlaMH4xCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJDQTEUMBIGA1UEBwwL%0AU2FudGEgQ2xhcmExGjAYBgNVBAoMEUludGVsIENvcnBvcmF0aW9uMTAwLgYDVQQD%0ADCdJbnRlbCBTR1ggQXR0ZXN0YXRpb24gUmVwb3J0IFNpZ25pbmcgQ0EwggGiMA0G%0ACSqGSIb3DQEBAQUAA4IBjwAwggGKAoIBgQCfPGR%2BtXc8u1EtJzLA10Feu1Wg%2Bp7e%0ALmSRmeaCHbkQ1TF3Nwl3RmpqXkeGzNLd69QUnWovYyVSndEMyYc3sHecGgfinEeh%0ArgBJSEdsSJ9FpaFdesjsxqzGRa20PYdnnfWcCTvFoulpbFR4VBuXnnVLVzkUvlXT%0AL%2FTAnd8nIZk0zZkFJ7P5LtePvykkar7LcSQO85wtcQe0R1Raf%2FsQ6wYKaKmFgCGe%0ANpEJUmg4ktal4qgIAxk%2BQHUxQE42sxViN5mqglB0QJdUot%2Fo9a%2FV%2FmMeH8KvOAiQ%0AbyinkNndn%2BBgk5sSV5DFgF0DffVqmVMblt5p3jPtImzBIH0QQrXJq39AT8cRwP5H%0AafuVeLHcDsRp6hol4P%2BZFIhu8mmbI1u0hH3W%2F0C2BuYXB5PC%2B5izFFh%2FnP0lc2Lf%0A6rELO9LZdnOhpL1ExFOq9H%2FB8tPQ84T3Sgb4nAifDabNt%2Fzu6MmCGo5U8lwEFtGM%0ARoOaX4AS%2B909x00lYnmtwsDVWv9vBiJCXRsCAwEAAaOByTCBxjBgBgNVHR8EWTBX%0AMFWgU6BRhk9odHRwOi8vdHJ1c3RlZHNlcnZpY2VzLmludGVsLmNvbS9jb250ZW50%0AL0NSTC9TR1gvQXR0ZXN0YXRpb25SZXBvcnRTaWduaW5nQ0EuY3JsMB0GA1UdDgQW%0ABBR4Q3t2pn680K9%2BQjfrNXw7hwFRPDAfBgNVHSMEGDAWgBR4Q3t2pn680K9%2BQjfr%0ANXw7hwFRPDAOBgNVHQ8BAf8EBAMCAQYwEgYDVR0TAQH%2FBAgwBgEB%2FwIBADANBgkq%0AhkiG9w0BAQsFAAOCAYEAeF8tYMXICvQqeXYQITkV2oLJsp6J4JAqJabHWxYJHGir%0AIEqucRiJSSx%2BHjIJEUVaj8E0QjEud6Y5lNmXlcjqRXaCPOqK0eGRz6hi%2BripMtPZ%0AsFNaBwLQVV905SDjAzDzNIDnrcnXyB4gcDFCvwDFKKgLRjOB%2FWAqgscDUoGq5ZVi%0AzLUzTqiQPmULAQaB9c6Oti6snEFJiCQ67JLyW%2FE83%2FfrzCmO5Ru6WjU4tmsmy8Ra%0AUd4APK0wZTGtfPXU7w%2BIBdG5Ez0kE1qzxGQaL4gINJ1zMyleDnbuS8UicjJijvqA%0A152Sq049ESDz%2B1rRGc2NVEqh1KaGXmtXvqxXcTB%2BLjy5Bw2ke0v8iGngFBPqCTVB%0A3op5KBG3RjbF6RRSzwzuWfL7QErNC8WEy5yDVARzTA5%2BxmBc388v9Dm21HGfcC8O%0ADD%2BgT9sSpssq0ascmvH49MOgjt1yoysLtdCtJW%2F9FZpoOypaHx0R%2BmJTLwPXVMrv%0ADaVzWh5aiEx%2BidkSGMnX%0A-----END%20CERTIFICATE-----%0A
Date: Mon, 21 Nov 2022 20:46:12 GMT
Connection: close

{"id":"30269556922087116282920178870493890659","timestamp":"2022-11-21T20:46:12.479104","version":3,"isvEnclaveQuoteStatus":"OK","isvEnclaveQuoteBody":"AgAAAEsMAAANAA0AAAAAAC9GSPlu9PnNQz0bjbjDPjhUxSAKFxTqVEPKCLDUH32aExMCB/+ABgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABwAAAAAAAAAHAAAAAAAAACulRC4tliigpbA4CYa+807lIlyroA5z/qKUszbsQ1LrAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACD1xnnferKFHD2uvYqTXdDA8iZ22kCD5xw7h38CMfOngAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAADtJ7eiAFZY0X8OshsSb4gzxHkR7jK+T6YiG8T3bwD0ZBzrM84ZNbceCHd0qz2po4rH1uHrHkYUp3sh39bAuJKL"}
parse_response_attn_report
parse result Ok(Complete(4807))
OK Operation Successful
content length = 730
Attestation report: {"id":"30269556922087116282920178870493890659","timestamp":"2022-11-21T20:46:12.479104","version":3,"isvEnclaveQuoteStatus":"OK","isvEnclaveQuoteBody":"AgAAAEsMAAANAA0AAAAAAC9GSPlu9PnNQz0bjbjDPjhUxSAKFxTqVEPKCLDUH32aExMCB/+ABgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABwAAAAAAAAAHAAAAAAAAACulRC4tliigpbA4CYa+807lIlyroA5z/qKUszbsQ1LrAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACD1xnnferKFHD2uvYqTXdDA8iZ22kCD5xw7h38CMfOngAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAADtJ7eiAFZY0X8OshsSb4gzxHkR7jK+T6YiG8T3bwD0ZBzrM84ZNbceCHd0qz2po4rH1uHrHkYUp3sh39bAuJKL"}
server cert: [Certificate(b"0\x82\x0b\x940\x82\x0b:\xa0\x03\x02\x01\x02\x02\x01\x010\n\x06\x08*\x86H\xce=\x04\x03\x020\x121\x100\x0e\x06\x03U\x04\x03\x0c\x07MesaTEE0\x1e\x17\r221121204612Z\x17\r230219204612Z0\x121\x100\x0e\x06\x03U\x04\x03\x0c\x07MesaTEE0Y0\x13\x06\x07*\x86H\xce=\x02\x01\x06\x08*\x86H\xce=\x03\x01\x07\x03B\0\x042\x1f:3`!N\x9b\xb6O\x06\x0b\xc5\xd9\x15\xf8Z\xa3\xd3{\x93\x96\xeb\xeb0\x0e\x9a\xce\x87\x87\xaa4]\xee\xafUh*\re\x84\x9b\xa6\0\x10I\xaf\xb76-\xbb\xfc\xc7'\x1c\x91\x99z\xc9\xee\x974qC\xa3\x82\n\x7f0\x82\n{0\x82\nw\x06\t`\x86H\x01\x86\xf8B\x01\r\x04\x82\nh{\"id\":\"39764797212119215723162443106314571679\",\"timestamp\":\"2022-11-21T20:46:12.280427\",\"version\":3,\"isvEnclaveQuoteStatus\":\"OK\",\"isvEnclaveQuoteBody\":\"AgAAAEsMAAANAA0AAAAAAC9GSPlu9PnNQz0bjbjDPjjtQL9vqwxxt49o3Q6etxHnExMCB/+ABgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABwAAAAAAAAAHAAAAAAAAACulRC4tliigpbA4CYa+807lIlyroA5z/qKUszbsQ1LrAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACD1xnnferKFHD2uvYqTXdDA8iZ22kCD5xw7h38CMfOngAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAyHzozYCFOm7ZPBgvF2RX4WqPTe5OW6+swDprOh4eqNF3ur1VoKg1lhJumABBJr7c2Lbv8xycckZl6ye6XNHFD\"}|NbaBL+DB8+GwWV43VnrwV6+Hzp9cmwQyURcW0OBeZ6gD7B3z3dsINIjKZmRClnweYK7lsBFKsUEa9zM/9lq2o7MvNrmR2XUqdI3Jp2PsFaMfTNVy2XTN/SSNRGFd0ycNpQVEcnv8UiPBH0tH9/BhTdSrp6kMOaTAf9nVh3ZCYhX5i4Ut2hAPN1La5KQVeyTYQcz9HSxUcLKfBk5qpNxO81nGAZCqpBokD1GurIJgJjJNUwZKTJvREWHYn/egS5G56YkTqK0MXuzHBGk3djMkr6SRAMERL+Kz30DygnzA8xSdX4WFLdVEnp+XwgL5SNzeoAuLFuTVJUMR6Z6IHsstQA==|MIIEoTCCAwmgAwIBAgIJANEHdl0yo7CWMA0GCSqGSIb3DQEBCwUAMH4xCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJDQTEUMBIGA1UEBwwLU2FudGEgQ2xhcmExGjAYBgNVBAoMEUludGVsIENvcnBvcmF0aW9uMTAwLgYDVQQDDCdJbnRlbCBTR1ggQXR0ZXN0YXRpb24gUmVwb3J0IFNpZ25pbmcgQ0EwHhcNMTYxMTIyMDkzNjU4WhcNMjYxMTIwMDkzNjU4WjB7MQswCQYDVQQGEwJVUzELMAkGA1UECAwCQ0ExFDASBgNVBAcMC1NhbnRhIENsYXJhMRowGAYDVQQKDBFJbnRlbCBDb3Jwb3JhdGlvbjEtMCsGA1UEAwwkSW50ZWwgU0dYIEF0dGVzdGF0aW9uIFJlcG9ydCBTaWduaW5nMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAqXot4OZuphR8nudFrAFiaGxxkgma/Es/BA+tbeCTUR106AL1ENcWA4FX3K+E9BBL0/7X5rj5nIgX/R/1ubhkKWw9gfqPG3KeAtIdcv/uTO1yXv50vqaPvE1CRChvzdS/ZEBqQ5oVvLTPZ3VEicQjlytKgN9cLnxbwtuvLUK7eyRPfJW/ksddOzP8VBBniolYnRCD2jrMRZ8nBM2ZWYwnXnwYeOAHV+W9tOhAImwRwKF/95yAsVwd21ryHMJBcGH70qLagZ7Ttyt++qO/6+KAXJuKwZqjRlEtSEz8gZQeFfVYgcwSfo96oSMAzVr7V0L6HSDLRnpb6xxmbPdqNol4tQIDAQABo4GkMIGhMB8GA1UdIwQYMBaAFHhDe3amfrzQr35CN+s1fDuHAVE8MA4GA1UdDwEB/wQEAwIGwDAMBgNVHRMBAf8EAjAAMGAGA1UdHwRZMFcwVaBToFGGT2h0dHA6Ly90cnVzdGVkc2VydmljZXMuaW50ZWwuY29tL2NvbnRlbnQvQ1JML1NHWC9BdHRlc3RhdGlvblJlcG9ydFNpZ25pbmdDQS5jcmwwDQYJKoZIhvcNAQELBQADggGBAGcIthtcK9IVRz4rRq+ZKE+7k50/OxUsmW8aavOzKb0iCx07YQ9rzi5nU73tME2yGRLzhSViFs/LpFa9lpQL6JL1aQwmDR74TxYGBAIi5f4I5TJoCCEqRHz91kpG6Uvyn2tLmnIdJbPE4vYvWLrtXXfFBSSPD4Afn7+3/XUggAlc7oCTizOfbbtOFlYA4g5KcYgS1J2ZAeMQqbUdZseZCcaZZZn65tdqee8UXZlDvx0+NdO0LR+5pFy+juM0wWbu59MvzcmTXbjsi7HY6zd53Yq5K244fwFHRQ8eOB0IWB+4PfM7FeAApZvlfqlKOlLcZL2uyVmzRkyR5yW72uo9mehX44CiPJ2fse9Y6eQtcfEhMPkmHXI01sN+KwPbpA39+xOsStjhP9N1Y1a2tQAVo+yVgLgV2Hws73Fc0o3wC78qPEA+v2aRs/Be3ZFDgDyghc/1fgU+7C+P6kbqd4poyb6IW8KCJbxfMJvkordNOgOUUxndPHEi/tb/U7uLjLOgPA==0\n\x06\x08*\x86H\xce=\x04\x03\x02\x03H\00E\x02 *\xc1\x19\xfc4\x99\x9bMD\xe9ko\xa5\xdd\xf3\x14\x03\x1d\x8cX\xb5\x1d#(&\xa4\xda\x81F\x94\0\xe6\x02!\0\xe3\\\x14\xee\xf2\xf4\xc1\x02\xa5\xff\xfau\x14\x80\x918\x02\xa9@\xafw\x8e\xfd\xb7\x10\x907\xff}\x85n,")]
Cert is good
Signature good
Time diff = 0
isvEnclaveQuoteStatus = OK
Quote = [2, 0, 0, 0, 75, 12, 0, 0, 13, 0, 13, 0, 0, 0, 0, 0, 47, 70, 72, 249, 110, 244, 249, 205, 67, 61, 27, 141, 184, 195, 62, 56, 237, 64, 191, 111, 171, 12, 113, 183, 143, 104, 221, 14, 158, 183, 17, 231, 19, 19, 2, 7, 255, 128, 6, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 7, 0, 0, 0, 0, 0, 0, 0, 7, 0, 0, 0, 0, 0, 0, 0, 43, 165, 68, 46, 45, 150, 40, 160, 165, 176, 56, 9, 134, 190, 243, 78, 229, 34, 92, 171, 160, 14, 115, 254, 162, 148, 179, 54, 236, 67, 82, 235, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 131, 215, 25, 231, 125, 234, 202, 20, 112, 246, 186, 246, 42, 77, 119, 67, 3, 200, 153, 219, 105, 2, 15, 156, 112, 238, 29, 252, 8, 199, 206, 158, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 50, 31, 58, 51, 96, 33, 78, 155, 182, 79, 6, 11, 197, 217, 21, 248, 90, 163, 211, 123, 147, 150, 235, 235, 48, 14, 154, 206, 135, 135, 170, 52, 93, 238, 175, 85, 104, 42, 13, 101, 132, 155, 166, 0, 16, 73, 175, 183, 54, 45, 187, 252, 199, 39, 28, 145, 153, 122, 201, 238, 151, 52, 113, 67]
sgx quote version = 2
sgx quote signature type = 0
sgx quote report_data = 321f3a3360214e9bb64f060bc5d915f85aa3d37b9396ebeb300e9ace8787aa345deeaf55682a0d65849ba6001049afb7362dbbfcc7271c91997ac9ee97347143
sgx quote mr_enclave = 2ba5442e2d9628a0a5b0380986bef34ee5225caba00e73fea294b336ec4352eb
sgx quote mr_signer = 83d719e77deaca1470f6baf62a4d774303c899db69020f9c70ee1dfc08c7ce9e
Anticipated public key = 321f3a3360214e9bb64f060bc5d915f85aa3d37b9396ebeb300e9ace8787aa345deeaf55682a0d65849ba6001049afb7362dbbfcc7271c91997ac9ee97347143
Mutual RA done!
Server replied: hello back
ECALL success!
[+] Done!
```