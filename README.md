# <div align="center"> PCF: A Progressive and Corrective Feedback for Latent Fingerprint Enhancement </div>

We understand the importance of transparency and reproducibility in research. To ensure a user-friendly experience, we are sharing the executable file. However, variations in environments can cause differences in results. Therefore, we also provide the results of NIST SD27, NIST SD302, IIITD MOLF, and IIITD MSLFD on [https://skconan.github.io/SFP-Progressive-Feedback-Latent-Fingerprint-Restoration](https://skconan.github.io/SFP-Progressive-Feedback-Latent-Fingerprint-Restoration/).


## <div align="left">Requirements</div>
 
- Windows 10 or 11 operating system.

- Storage 14 GB 
    
    - ksip_lfp_enh_installer 300 MB
    - MATLAB_Runtime_R2022a_Update_6_win64 (installer 4 GB and install space required 8 GB)


<br/>

## <div align="left">Installation</div>

### Install MATLAB Runtime version R2022a (9.12)

1. Download MATLAB Runtime from [www.mathworks.com](https://www.mathworks.com/products/compiler/matlab-runtime.html) Or [MATLAB_Runtime_R2022a_Update_6_win64.zip](https://drive.google.com/file/d/1UGLNieWDnR3yDj5UOEOA-MRmD9vIVjfA/view?usp=sharing)</b>.

2. Extract files and install MATLAB Runtime using `setup.exe`.

### Install KSIP Latent Fingerprint Enhancement

1. Download [ksip_lfp_enh_installer.exe](https://drive.google.com/file/d/1XMiQDv1-4gyGhQQmsdIZbsQh8z3kMkMS/view?usp=sharing)</b>.

2. Install `KSIP LFP ENHANCEMENT` using `ksip_lfp_enh_installer.exe`. The installation directory will be `C:\Program Files (x86)\KSIP LFP ENHANCEMENT`

3. Setup environment path 
	- Go to `Environment Variables`
	- Add `C:\Program Files (x86)\KSIP LFP ENHANCEMENT` in the `Path` variable under System variables. 

    If KSIP LFP ENHANCEMENT installed in a different location, add that specific path to System variables instead of C:\Program Files (x86)\KSIP LFP ENHANCEMENT.


<br/>

## <div align="left">Usage</div>

### Preprocessing

Before performing fingerprint enhancement, the texture image needs to be extracted using [Total Variation](https://www.mathworks.com/matlabcentral/fileexchange/43600-deconvtv-fast-algorithm-for-total-variation-deconvolution). Note use `mu` is 0.45. Ensure you have completed this step before proceeding with the enhancement process.


### Enhancement

1. Open `Terminal` or `Windows Powershell`

2. Run `ksip_pcf.exe <org_dir> <tv_dir> <seg_dir> <out_dir>` and Enter. 

        usage: ksip_pcf.exe <org_dir> <tv_dir> <seg_dir> <out_dir>

        arguments:
        
        <org_dir>     Original Fingerprint Image Directory
        <tv_dir>      Fingerprint Total Variation Directory
        <seg_dir>     Segment Directory
        <out_dir>     Output Directory
	
### Example

- Run NIST SD27 Enhancement

		ksip_pcf.exe D:\NIST_SD27\Latent D:\NIST_SD27\LatentTV D:\NIST_SD27\GlobalDict  D:\NIST_SD27\Enhancement

### Output Example

    Original Fingerprint Image DIrectory: D:\NIST_SD27\Latent
    Fingerprint TV Image DIrectory: D:\NIST_SD27\LatentTV
    Fingerprint Segment DIrectory: D:\NIST_SD27\GlobalDict
    Fingerprint Enhanced DIrectory: D:\NIST_SD27\Enhancement
    0001/0002 Start enhancement: 001L2U.bmp
    0001/0002 Enhancement Success
    0001/0002 Save enhanced image to D:\NIST_SD27\Enhancement\001L2U.bmp
    0001/0002 Execution time: 25.36 second

<br/>

## <div align="left"> Acknowledgements </div>

This work was supported in part by the Department of Electrical Engineering, Faculty of Engineering, Kasetsart University, and in part by the Siew-Sngiem Karnchanachari Research Leadership and Young Professorship Awards.

<br/>


## <div align="left">License</div>

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.

<br/>


## <div align="left">Citing PCF</div>

If you are using PCF or benchmarks in your research, kindly reference the following.


    @ARTICLE{9469797,
        author={Horapong, Kittipol and Srisutheenon, Kittinuth and Areekul, Vutipong},
        journal={IEEE Access}, 
        title={Progressive and Corrective Feedback for Latent Fingerprint Enhancement Using Boosted Spectral Filtering and Spectral Autoencoder}, 
        year={2021},
        volume={9},
        number={},
        pages={96288-96308},
        doi={10.1109/ACCESS.2021.3093879}
    }

Or

    K. Horapong, K. Srisutheenon and V. Areekul, "Progressive and Corrective Feedback for Latent Fingerprint Enhancement Using Boosted Spectral Filtering and Spectral Autoencoder," in IEEE Access, vol. 9, pp. 96288-96308, 2021, doi: 10.1109/ACCESS.2021.3093879.


<br/>

## <div align="left">Contact</div>

If you have any questions or need assistance, reach us at fengvpa@ku.ac.th / kttpl@hotmail.com / kittipol.h@ku.th.
