<p align="center">
  <a href="#build-framework">
   <img src="https://raw.githubusercontent.com/armbian/build/master/.github/armbian-logo.png" alt="Armbian logo" width="144">
  </a><br>
  <strong>Armbian OS</strong><br>
<br>
<a href=https://github.com/armbian/os/actions/workflows/complete-artifact-matrix-all.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/complete-artifact-matrix-all.yml?logo=githubactions&label=Artifacts%20make&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os/actions/workflows/repository-update.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/repository-update.yml?logo=githubactions&label=Repository%20update&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os#latest-smoke-tests-results><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/smoke-tests.yml?logo=githubactions&label=Smoke%20tests&style=for-the-badge&branch=main"></a>
</p>


# What does this project do?

- Keeps build framework [packages artifacts](https://github.com/orgs/armbian/packages) cache up to date
- Keeps stable [apt.armbian.com](https://apt.armbian.com) and nightly [beta.armbian.com](https://beta.armbian.com) packages repository up to date
- Builds [nightly](https://github.com/armbian/os/releases) and [stable images](https://www.armbian.com/download/) and uploads them to Armbian CDN
- Keep synchronizing the selection of [3rd party](external) applications with Armbian repositories
- Tests install of all packages added onto stable and testing Debian and Ubuntu releases

# How to enable images?

If you want to enable build configurations, edit [yaml config files](userpatches) and send a pull request. ([example](https://github.com/armbian/os/commit/70f3be4f3d96e9a301be751d3ecf3a24394356f9) )

# When is this happening?

- Artifacts cache is updated every eight hours, starting at 0:00 AM UTC
- Repository update starts after **artifacts cache update** is done succesfully.
- Smoke tests starts **manually**.
- Nightly images are build once per day, at 2:00 AM UTC, or if [build config is changed](https://github.com/armbian/os/blob/main/userpatches/targets-release-nightly.yaml)
- Manually, when Armbian [release manager](https://github.com/orgs/armbian/teams/release-manager) executes a build action

# Latest smoke tests results:

- installs kernels, dtb and headers that are defined and supported by the board
- runs network and computing performance tests (7z benchmark)
- store armbianmonitor logs

<!--START_SECTION:data-section-->
<table width="100%"><tr><td align="left"><a id=Board ID href=#Board ID><b>Board name</b></a></td><td align=left><b>Logs</b></td><td align=right><b>Branch</b></td><td align=right><b>Iperf</b></td><td align=right><b>7z -b</b></td><td align=right><b>Repo</b></td></tr><tr><td align="left"><a id=zeropi href=#zeropi>ZeroPi</a></td><td align=left>https://paste.armbian.com/awubelahic</td><td align=right>legacy</td><td align=right>531</td><td align=right>2652</td><td align=right>beta</td></tr><tr><td align="left"><a id=zeropi href=#zeropi>ZeroPi</a></td><td align=left>https://paste.armbian.com/arevupolup</td><td align=right>legacy</td><td align=right>546</td><td align=right>2655</td><td align=right>stable</td></tr><tr><td align="left"><a id=lepotato href=#lepotato>Le potato</a></td><td align=left>https://paste.armbian.com/qulewozici</td><td align=right>current</td><td align=right>88</td><td align=right>3800</td><td align=right>beta</td></tr><tr><td align="left"><a id=lepotato href=#lepotato>Le potato</a></td><td align=left>https://paste.armbian.com/debamiduke</td><td align=right>current</td><td align=right>93</td><td align=right>3801</td><td align=right>stable</td></tr><tr><td align="left"><a id=lepotato href=#lepotato>Le potato</a></td><td align=left>https://paste.armbian.com/mexibepilo</td><td align=right>edge</td><td align=right>91</td><td align=right>3802</td><td align=right>beta</td></tr><tr><td align="left"><a id=lepotato href=#lepotato>Le potato</a></td><td align=left>https://paste.armbian.com/axotadosub</td><td align=right>edge</td><td align=right>90</td><td align=right>3799</td><td align=right>stable</td></tr><tr><td align="left"><a id=bananapim5 href=#bananapim5>Banana Pi M5</a></td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=bananapim5 href=#bananapim5>Banana Pi M5</a></td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=bananapim5 href=#bananapim5>Banana Pi M5</a></td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=bananapim5 href=#bananapim5>Banana Pi M5</a></td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidm1 href=#odroidm1>ODROID M1</a></td><td align=left>https://paste.armbian.com/vurosuhebe</td><td align=right>edge</td><td align=right>890</td><td align=right>5339</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidm1 href=#odroidm1>ODROID M1</a></td><td align=left>https://paste.armbian.com/mufecasula</td><td align=right>edge</td><td align=right>920</td><td align=right>5361</td><td align=right>stable</td></tr><tr><td align="left"><a id=orangepi5 href=#orangepi5>Orange Pi 5</a></td><td align=left>https://paste.armbian.com/ijinezufis</td><td align=right>legacy</td><td align=right>970</td><td align=right>15653</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepi5 href=#orangepi5>Orange Pi 5</a></td><td align=left>https://paste.armbian.com/nupokaruro</td><td align=right>legacy</td><td align=right>880</td><td align=right>15522</td><td align=right>stable</td></tr><tr><td align="left"><a id=nanopineo3 href=#nanopineo3>NanoPi Neo 3</a></td><td align=left>https://paste.armbian.com/etepuhumuk</td><td align=right>current</td><td align=right>800</td><td align=right>3507</td><td align=right>beta</td></tr><tr><td align="left"><a id=nanopineo3 href=#nanopineo3>NanoPi Neo 3</a></td><td align=left>https://paste.armbian.com/yoqiwomeri</td><td align=right>current</td><td align=right>900</td><td align=right>3175</td><td align=right>stable</td></tr><tr><td align="left"><a id=nanopineo3 href=#nanopineo3>NanoPi Neo 3</a></td><td align=left>https://paste.armbian.com/bacewovefa</td><td align=right>edge</td><td align=right>890</td><td align=right>2957</td><td align=right>beta</td></tr><tr><td align="left"><a id=nanopineo3 href=#nanopineo3>NanoPi Neo 3</a></td><td align=left>https://paste.armbian.com/jikoviwidi</td><td align=right>edge</td><td align=right>814</td><td align=right>2903</td><td align=right>stable</td></tr><tr><td align="left"><a id=bananapim2ultra href=#bananapim2ultra>Banana Pi M2 Ultra</a></td><td align=left>https://paste.armbian.com/kiciceceki</td><td align=right>current</td><td align=right>855</td><td align=right>2723</td><td align=right>beta</td></tr><tr><td align="left"><a id=bananapim2ultra href=#bananapim2ultra>Banana Pi M2 Ultra</a></td><td align=left>https://paste.armbian.com/awevazutac</td><td align=right>current</td><td align=right>778</td><td align=right>2715</td><td align=right>stable</td></tr><tr><td align="left"><a id=pineh64 href=#pineh64>Pine H64</a></td><td align=left>https://paste.armbian.com/jicayequlo</td><td align=right>current</td><td align=right>800</td><td align=right>4210</td><td align=right>beta</td></tr><tr><td align="left"><a id=pineh64 href=#pineh64>Pine H64</a></td><td align=left>https://paste.armbian.com/miqihugede</td><td align=right>current</td><td align=right>915</td><td align=right>4093</td><td align=right>stable</td></tr><tr><td align="left"><a id=pineh64 href=#pineh64>Pine H64</a></td><td align=left>https://paste.armbian.com/asibecisez</td><td align=right>edge</td><td align=right>840</td><td align=right>4016</td><td align=right>beta</td></tr><tr><td align="left"><a id=pineh64 href=#pineh64>Pine H64</a></td><td align=left>https://paste.armbian.com/enimojaluj</td><td align=right>edge</td><td align=right>816</td><td align=right>4004</td><td align=right>stable</td></tr><tr><td align="left"><a id=uefi-x86 href=#uefi-x86>UEFI x86</a></td><td align=left>https://paste.armbian.com/wapiherozi</td><td align=right>legacy</td><td align=right>890</td><td align=right>4809</td><td align=right>beta</td></tr><tr><td align="left"><a id=uefi-x86 href=#uefi-x86>UEFI x86</a></td><td align=left>https://paste.armbian.com/pepetuneca</td><td align=right>legacy</td><td align=right>870</td><td align=right>4862</td><td align=right>stable</td></tr><tr><td align="left"><a id=uefi-x86 href=#uefi-x86>UEFI x86</a></td><td align=left>https://paste.armbian.com/uzomidowiv</td><td align=right>current</td><td align=right>840</td><td align=right>4789</td><td align=right>beta</td></tr><tr><td align="left"><a id=uefi-x86 href=#uefi-x86>UEFI x86</a></td><td align=left>https://paste.armbian.com/zohesiqapo</td><td align=right>current</td><td align=right>873</td><td align=right>4807</td><td align=right>stable</td></tr><tr><td align="left"><a id=uefi-x86 href=#uefi-x86>UEFI x86</a></td><td align=left>https://paste.armbian.com/sanajemaho</td><td align=right>edge</td><td align=right>869</td><td align=right>4880</td><td align=right>beta</td></tr><tr><td align="left"><a id=uefi-x86 href=#uefi-x86>UEFI x86</a></td><td align=left>https://paste.armbian.com/bahejasoku</td><td align=right>edge</td><td align=right>866</td><td align=right>4788</td><td align=right>stable</td></tr><tr><td align="left"><a id=khadas-vim3 href=#khadas-vim3>Khadas VIM3</a></td><td align=left>https://paste.armbian.com/ezetuwajol</td><td align=right>current</td><td align=right>970</td><td align=right>9633</td><td align=right>beta</td></tr><tr><td align="left"><a id=khadas-vim3 href=#khadas-vim3>Khadas VIM3</a></td><td align=left>https://paste.armbian.com/osikigunuw</td><td align=right>current</td><td align=right>890</td><td align=right>9542</td><td align=right>stable</td></tr><tr><td align="left"><a id=khadas-vim3 href=#khadas-vim3>Khadas VIM3</a></td><td align=left>https://paste.armbian.com/xobekiyozo</td><td align=right>edge</td><td align=right>730</td><td align=right>9415</td><td align=right>beta</td></tr><tr><td align="left"><a id=khadas-vim3 href=#khadas-vim3>Khadas VIM3</a></td><td align=left>n/a</td><td align=right>edge</td><td align=right>0</td><td align=right>9519</td><td align=right>stable</td></tr><tr><td align="left"><a id=rockpi-e href=#rockpi-e>Rockpi E</a></td><td align=left>https://paste.armbian.com/ihetijeqaf</td><td align=right>current</td><td align=right>800</td><td align=right>3401</td><td align=right>beta</td></tr><tr><td align="left"><a id=rockpi-e href=#rockpi-e>Rockpi E</a></td><td align=left>https://paste.armbian.com/uhejebohom</td><td align=right>current</td><td align=right>88</td><td align=right>3398</td><td align=right>stable</td></tr><tr><td align="left"><a id=rockpi-e href=#rockpi-e>Rockpi E</a></td><td align=left>https://paste.armbian.com/elujevodax</td><td align=right>edge</td><td align=right>90</td><td align=right>3305</td><td align=right>beta</td></tr><tr><td align="left"><a id=rockpi-e href=#rockpi-e>Rockpi E</a></td><td align=left>https://paste.armbian.com/furulorade</td><td align=right>edge</td><td align=right>89</td><td align=right>3392</td><td align=right>stable</td></tr><tr><td align="left"><a id=rockpi-4b href=#rockpi-4b>Rockpi 4B</a></td><td align=left>https://paste.armbian.com/uxewiyiyev</td><td align=right>current</td><td align=right>830</td><td align=right>6394</td><td align=right>beta</td></tr><tr><td align="left"><a id=rockpi-4b href=#rockpi-4b>Rockpi 4B</a></td><td align=left>https://paste.armbian.com/ozacorufed</td><td align=right>current</td><td align=right>939</td><td align=right>6186</td><td align=right>stable</td></tr><tr><td align="left"><a id=rockpi-4b href=#rockpi-4b>Rockpi 4B</a></td><td align=left>https://paste.armbian.com/dikalanaze</td><td align=right>edge</td><td align=right>970</td><td align=right>6121</td><td align=right>beta</td></tr><tr><td align="left"><a id=rockpi-4b href=#rockpi-4b>Rockpi 4B</a></td><td align=left>https://paste.armbian.com/cekeqezufu</td><td align=right>edge</td><td align=right>970</td><td align=right>6148</td><td align=right>stable</td></tr><tr><td align="left"><a id=khadas-vim2 href=#khadas-vim2>Khadas VIM2</a></td><td align=left>https://paste.armbian.com/ozumujojok</td><td align=right>current</td><td align=right>910</td><td align=right>6226</td><td align=right>beta</td></tr><tr><td align="left"><a id=khadas-vim2 href=#khadas-vim2>Khadas VIM2</a></td><td align=left>https://paste.armbian.com/okugemakip</td><td align=right>current</td><td align=right>890</td><td align=right>6206</td><td align=right>stable</td></tr><tr><td align="left"><a id=khadas-vim2 href=#khadas-vim2>Khadas VIM2</a></td><td align=left>https://paste.armbian.com/vovixumove</td><td align=right>edge</td><td align=right>910</td><td align=right>6074</td><td align=right>beta</td></tr><tr><td align="left"><a id=khadas-vim2 href=#khadas-vim2>Khadas VIM2</a></td><td align=left>https://paste.armbian.com/umogukonew</td><td align=right>edge</td><td align=right>910</td><td align=right>6203</td><td align=right>stable</td></tr><tr><td align="left"><a id=khadas-vim1 href=#khadas-vim1>Khadas VIM1</a></td><td align=left>https://paste.armbian.com/agecigekab</td><td align=right>current</td><td align=right>98</td><td align=right>3722</td><td align=right>beta</td></tr><tr><td align="left"><a id=khadas-vim1 href=#khadas-vim1>Khadas VIM1</a></td><td align=left>https://paste.armbian.com/zelanexaco</td><td align=right>current</td><td align=right>90</td><td align=right>3720</td><td align=right>stable</td></tr><tr><td align="left"><a id=khadas-vim1 href=#khadas-vim1>Khadas VIM1</a></td><td align=left>https://paste.armbian.com/vivasabotu</td><td align=right>edge</td><td align=right>96</td><td align=right>3724</td><td align=right>beta</td></tr><tr><td align="left"><a id=khadas-vim1 href=#khadas-vim1>Khadas VIM1</a></td><td align=left>https://paste.armbian.com/uwaticozez</td><td align=right>edge</td><td align=right>101</td><td align=right>3725</td><td align=right>stable</td></tr><tr><td align="left"><a id=bigtreetech-cb1 href=#bigtreetech-cb1>BigTreeTech CB1</a></td><td align=left>https://paste.armbian.com/uqebijawub</td><td align=right>legacy</td><td align=right>92</td><td align=right>2702</td><td align=right>beta</td></tr><tr><td align="left"><a id=bigtreetech-cb1 href=#bigtreetech-cb1>BigTreeTech CB1</a></td><td align=left>https://paste.armbian.com/azijurewit</td><td align=right>legacy</td><td align=right>90</td><td align=right>2614</td><td align=right>stable</td></tr><tr><td align="left"><a id=orangepizero2 href=#orangepizero2>Orange Pi Zero2</a></td><td align=left>https://paste.armbian.com/itozerejut</td><td align=right>current</td><td align=right>830</td><td align=right>3140</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepizero2 href=#orangepizero2>Orange Pi Zero2</a></td><td align=left>https://paste.armbian.com/duganofuso</td><td align=right>current</td><td align=right>841</td><td align=right>3079</td><td align=right>stable</td></tr><tr><td align="left"><a id=orangepizero2 href=#orangepizero2>Orange Pi Zero2</a></td><td align=left>https://paste.armbian.com/nojixuvaqo</td><td align=right>edge</td><td align=right>830</td><td align=right>2997</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepizero2 href=#orangepizero2>Orange Pi Zero2</a></td><td align=left>https://paste.armbian.com/akizuwotiv</td><td align=right>edge</td><td align=right>832</td><td align=right>2985</td><td align=right>stable</td></tr><tr><td align="left"><a id=odroidc2 href=#odroidc2>Odroid C2</a></td><td align=left>https://paste.armbian.com/hohowaquka</td><td align=right>current</td><td align=right>880</td><td align=right>3891</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidc2 href=#odroidc2>Odroid C2</a></td><td align=left>https://paste.armbian.com/akayadotuh</td><td align=right>current</td><td align=right>890</td><td align=right>3974</td><td align=right>stable</td></tr><tr><td align="left"><a id=odroidc2 href=#odroidc2>Odroid C2</a></td><td align=left>https://paste.armbian.com/maqegefivi</td><td align=right>edge</td><td align=right>880</td><td align=right>4064</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidc2 href=#odroidc2>Odroid C2</a></td><td align=left>https://paste.armbian.com/efepadugaq</td><td align=right>edge</td><td align=right>874</td><td align=right>4071</td><td align=right>stable</td></tr><tr><td align="left"><a id=rockpro64 href=#rockpro64>RockPro 64</a></td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>beta</td></tr><tr><td align="left"><a id=rockpro64 href=#rockpro64>RockPro 64</a></td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>beta</td></tr><tr><td align="left"><a id=rockpro64 href=#rockpro64>RockPro 64</a></td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>beta</td></tr><tr><td align="left"><a id=rockpro64 href=#rockpro64>RockPro 64</a></td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidc4 href=#odroidc4>Odroid C4</a></td><td align=left>https://paste.armbian.com/bazeyiwoca</td><td align=right>current</td><td align=right>890</td><td align=right>5616</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidc4 href=#odroidc4>Odroid C4</a></td><td align=left>https://paste.armbian.com/ocufudufug</td><td align=right>current</td><td align=right>800</td><td align=right>5628</td><td align=right>stable</td></tr><tr><td align="left"><a id=odroidc4 href=#odroidc4>Odroid C4</a></td><td align=left>https://paste.armbian.com/xuyalorasi</td><td align=right>edge</td><td align=right>860</td><td align=right>5642</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidc4 href=#odroidc4>Odroid C4</a></td><td align=left>https://paste.armbian.com/imevivibij</td><td align=right>edge</td><td align=right>890</td><td align=right>5611</td><td align=right>stable</td></tr><tr><td align="left"><a id=orangepizero href=#orangepizero>Orange Pi Zero</a></td><td align=left>https://paste.armbian.com/rotamakibu</td><td align=right>current</td><td align=right>90</td><td align=right>2374</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepizero href=#orangepizero>Orange Pi Zero</a></td><td align=left>https://paste.armbian.com/ujebefileh</td><td align=right>current</td><td align=right>90</td><td align=right>2323</td><td align=right>stable</td></tr><tr><td align="left"><a id=orangepi-r1 href=#orangepi-r1>Orange Pi R1</a></td><td align=left>https://paste.armbian.com/apehugogon</td><td align=right>current</td><td align=right>90</td><td align=right>2728</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepi-r1 href=#orangepi-r1>Orange Pi R1</a></td><td align=left>https://paste.armbian.com/pexasojujo</td><td align=right>current</td><td align=right>89</td><td align=right>2677</td><td align=right>stable</td></tr><tr><td align="left"><a id=orangepi-r1 href=#orangepi-r1>Orange Pi R1</a></td><td align=left>https://paste.armbian.com/obopehanaf</td><td align=right>edge</td><td align=right>89</td><td align=right>2333</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepi-r1 href=#orangepi-r1>Orange Pi R1</a></td><td align=left>https://paste.armbian.com/imunucebux</td><td align=right>edge</td><td align=right>89</td><td align=right>2112</td><td align=right>stable</td></tr><tr><td align="left"><a id=orangepizeroplus href=#orangepizeroplus>Orange Pi Zero Plus</a></td><td align=left>https://paste.armbian.com/vomazizine</td><td align=right>current</td><td align=right>848</td><td align=right>2531</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepizeroplus href=#orangepizeroplus>Orange Pi Zero Plus</a></td><td align=left>https://paste.armbian.com/ejigaketax</td><td align=right>current</td><td align=right>780</td><td align=right>2523</td><td align=right>stable</td></tr><tr><td align="left"><a id=orangepizeroplus href=#orangepizeroplus>Orange Pi Zero Plus</a></td><td align=left>https://paste.armbian.com/socudapabu</td><td align=right>edge</td><td align=right>849</td><td align=right>2643</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepizeroplus href=#orangepizeroplus>Orange Pi Zero Plus</a></td><td align=left>https://paste.armbian.com/kacihoxoyi</td><td align=right>edge</td><td align=right>838</td><td align=right>2530</td><td align=right>stable</td></tr><tr><td align="left"><a id=tinkerboard href=#tinkerboard>Tinker Board</a></td><td align=left>https://paste.armbian.com/adogunehor</td><td align=right>current</td><td align=right>890</td><td align=right>5053</td><td align=right>beta</td></tr><tr><td align="left"><a id=tinkerboard href=#tinkerboard>Tinker Board</a></td><td align=left>https://paste.armbian.com/imunerubak</td><td align=right>current</td><td align=right>890</td><td align=right>4929</td><td align=right>stable</td></tr><tr><td align="left"><a id=tinkerboard-2 href=#tinkerboard-2>Tinker Board 2</a></td><td align=left>https://paste.armbian.com/catenunune</td><td align=right>current</td><td align=right>859</td><td align=right>6852</td><td align=right>beta</td></tr><tr><td align="left"><a id=tinkerboard-2 href=#tinkerboard-2>Tinker Board 2</a></td><td align=left>https://paste.armbian.com/onusoruzec</td><td align=right>current</td><td align=right>840</td><td align=right>6779</td><td align=right>stable</td></tr><tr><td align="left"><a id=odroidn2 href=#odroidn2>Odroid N2</a></td><td align=left>https://paste.armbian.com/ikuwumojec</td><td align=right>current</td><td align=right>907</td><td align=right>8923</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidn2 href=#odroidn2>Odroid N2</a></td><td align=left>https://paste.armbian.com/oremoyaquv</td><td align=right>current</td><td align=right>810</td><td align=right>8913</td><td align=right>stable</td></tr><tr><td align="left"><a id=odroidn2 href=#odroidn2>Odroid N2</a></td><td align=left>https://paste.armbian.com/axelogaxen</td><td align=right>edge</td><td align=right>890</td><td align=right>8587</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidn2 href=#odroidn2>Odroid N2</a></td><td align=left>https://paste.armbian.com/novojatujo</td><td align=right>edge</td><td align=right>960</td><td align=right>8763</td><td align=right>stable</td></tr><tr><td align="left"><a id=odroidxu4 href=#odroidxu4>Odroid XU4</a></td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidxu4 href=#odroidxu4>Odroid XU4</a></td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=bananapicm4io href=#bananapicm4io>Banana Pi CM4IO</a></td><td align=left>https://paste.armbian.com/tamukehori</td><td align=right>current</td><td align=right>890</td><td align=right>9389</td><td align=right>beta</td></tr><tr><td align="left"><a id=bananapicm4io href=#bananapicm4io>Banana Pi CM4IO</a></td><td align=left>https://paste.armbian.com/yipemolite</td><td align=right>current</td><td align=right>841</td><td align=right>8904</td><td align=right>stable</td></tr><tr><td align="left"><a id=bananapicm4io href=#bananapicm4io>Banana Pi CM4IO</a></td><td align=left>https://paste.armbian.com/qewegitago</td><td align=right>edge</td><td align=right>770</td><td align=right>8598</td><td align=right>beta</td></tr><tr><td align="left"><a id=bananapicm4io href=#bananapicm4io>Banana Pi CM4IO</a></td><td align=left>https://paste.armbian.com/qunodazila</td><td align=right>edge</td><td align=right>890</td><td align=right>8154</td><td align=right>stable</td></tr><tr><td align="left"><a id=udoo href=#udoo>Udoo</a></td><td align=left>https://paste.armbian.com/siroqexifa</td><td align=right>current</td><td align=right>334</td><td align=right>2344</td><td align=right>beta</td></tr><tr><td align="left"><a id=udoo href=#udoo>Udoo</a></td><td align=left>https://paste.armbian.com/araqizumod</td><td align=right>current</td><td align=right>333</td><td align=right>2353</td><td align=right>stable</td></tr><tr><td align="left"><a id=rock-5b href=#rock-5b>Rock 5B</a></td><td align=left>https://paste.armbian.com/pisijisave</td><td align=right>legacy</td><td align=right>2449</td><td align=right>15483</td><td align=right>beta</td></tr><tr><td align="left"><a id=rock-5b href=#rock-5b>Rock 5B</a></td><td align=left>https://paste.armbian.com/uquqiyowag</td><td align=right>legacy</td><td align=right>2266</td><td align=right>15642</td><td align=right>stable</td></tr><tr><td align="left"><a id=khadas-edge2 href=#khadas-edge2>Khadas Edge2</a></td><td align=left>https://paste.armbian.com/velomaqeji</td><td align=right>legacy</td><td align=right>110</td><td align=right>15479</td><td align=right>beta</td></tr><tr><td align="left"><a id=khadas-edge2 href=#khadas-edge2>Khadas Edge2</a></td><td align=left>https://paste.armbian.com/uzihamimiy</td><td align=right>legacy</td><td align=right>120</td><td align=right>15367</td><td align=right>stable</td></tr></table>
<!--END_SECTION:data-section-->

## Would you like to join spare hardware to this automated testings?

All you need to do is:

- deploy any latest Armbian image to hardware
- provide IP address
- [contact us](https://www.armbian.com/contact/)

Device has to be always on and easily accesible for you to re-image in case of failed upgrade.

## Development

- [Pull request](https://github.com/armbian/build/pulls)
- [Weekly developers meetings](https://forum.armbian.com/events/)
- [Forums for developers](https://forum.armbian.com/forum/4-advanced-users-development/)

## OS download

- [Download](https://www.armbian.com/download/)

## Support

- [Using Armbian](https://forum.armbian.com/forum/23-using-armbian/)

## Contact

- [Forums](https://forum.armbian.com) for Participate in Armbian
- IRC: `#armbian` on Libera.chat
- Discord: [https://discord.gg/armbian](https://discord.gg/armbian)
- Follow [@armbian](https://twitter.com/armbian) on Twitter, [Fosstodon](https://fosstodon.org/@armbian) or [LinkedIn](https://www.linkedin.com/company/armbian).
- Bugs: [issues](https://github.com/armbian/build/issues) / [JIRA](https://armbian.atlassian.net/jira/dashboards/10000)
- Office hours: [Wednesday, 12 midday, 18 afternoon, CET](https://calendly.com/armbian/office-hours)

## License

This software is published under the GPL-2.0 License license.
