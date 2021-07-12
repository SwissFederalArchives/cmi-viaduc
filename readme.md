
# cmi-viaduc

- **[cmi-viaduc](https://github.com/SwissFederalArchives/cmi-viaduc)** :triangular_flag_on_post:
  - [cmi-viaduc-web-core](https://github.com/SwissFederalArchives/cmi-viaduc-web-core)
  - [cmi-viaduc-web-frontend](https://github.com/SwissFederalArchives/cmi-viaduc-web-frontend)
  - [cmi-viaduc-web-management](https://github.com/SwissFederalArchives/cmi-viaduc-web-management)
  - [cmi-viaduc-backend](https://github.com/SwissFederalArchives/cmi-viaduc-backend)

# Introduction

_Viaduc_ originated as a development project for the online access of the Swiss Federal Archives (SFA). The online access of the SFA can be described as a digital reading room: it can handle most of the archive's public accessibility tasks on its digital platform (see the [platform's user manual](https://www.bar.admin.ch/dam/bar/en/dokumente/kundeninformation/Benutzerhandbuch-Webportal.pdf.download.pdf/Benutzerhandbuch-Webportal.pdf)).

Its hightlights comprise the following features:

- Search in public metadata and primary data.
- Search in protected meta- and primary data for authorized users.
- User authentification and differentiated levels of  access to metadata and primary data.
- Downloading primary data as a working copy, in DIP (Dissemination Information Package) structure.
- Ordering digital copies of archival records.
- Preparation of the working copy includes
  - OCR recognition of scans
  - Format conversion from archive to user formats
- Storage of public working copies in a cache
- Issuing requests for consultation of protected files
- Temporary access to documents by authorized persons upon request
- Government offices have access to their own documents
- Backend application for order management, consultation requests, administrative access and other settings.

In order for the archival community to benefit from the investment, knowledge and solutions to various problems, the SFA has decided to make the source code available.

# Overview

The complete solution of the online acces includes 4 code repositories.

The repository [cmi-viaduc-web-core](https://github.com/SwissFederalArchives/cmi-viaduc-web-core) is an Angular library.
This library is used by the other two applications,  Public Access  ([cmi-viaduc-web-frontend](https://github.com/SwissFederalArchives/cmi-viaduc-web-frontend)) and Internal Management ([cmi-viaduc-web-management](https://github.com/SwissFederalArchives/cmi-viaduc-web-management)), as a common code base and component library.
The frontend applications are hosted in an `ASP.NET` container (see backend repository [cmi-viaduc-backend](https://github.com/SwissFederalArchives/cmi-viaduc-backend)) and communicate with the system via a web API.

![The Big-Picture](docs/imgs/context.svg)

# Remarks
This code has been developed in the specific context of the Swiss Federal Archives. It includes in some places hard-coded links to several services used in this context, namely
 
- URLs to pages of other federal administration services ( *\.admin.ch ) 
- URLs to the public-client and to the management-client ( https://www.recherche.bar.admin.ch.*) 
- URLs to authentication services (E-IAM and Swisscom) ( https://www.recherche.bar.admin.ch/private | https://dis.swisscom.ch/* )
- URLs to chatbot and co-browsing services (https://chatbot.bar.smartive.cloud/* | https://unblu.cloud/unblu/* )

Replace them as needed to adapt the code to your specific environment.

# Authors

- [CM Informatik AG](https://cmiag.ch)
- [Evelix GmbH](https://evelix.ch)

# License

All repositories are licensed under the
GNU Affero General Public License (AGPLv3). See [LICENSE](LICENSE.TXT).

# Project status

The initial development project is finished; currently the online access of the SFA is in the maintenance/continuation phase. It is planned to make selective developments, corrections and improvements every year and to publish them here.

# Lines of Code
## cmi-viaduc-backend
[![](https://tokei.rs/b1/github/SwissFederalArchives/cmi-viaduc-backend)](https://github.com/SwissFederalArchives/cmi-viaduc-backend)

## cmi-viaduc-web-core
[![](https://tokei.rs/b1/github/SwissFederalArchives/cmi-viaduc-web-core)](https://github.com/SwissFederalArchives/cmi-viaduc-web-core)

## cmi-viaduc-web-management
[![](https://tokei.rs/b1/github/SwissFederalArchives/cmi-viaduc-web-management)](https://github.com/SwissFederalArchives/cmi-viaduc-web-management)

## cmi-viaduc-web-frontend
[![](https://tokei.rs/b1/github/SwissFederalArchives/cmi-viaduc-web-frontend)](https://github.com/SwissFederalArchives/cmi-viaduc-web-frontend)

# Contribute

This repository is a copy which will be updated regularly - therefore contributions via pull requests are not possible. However, independent copies (forks) are possible under consideration of the AGPLV3 license.

# Contact

- For general questions (and technical support), please contact the Swiss Federal Archives by e-mail at info@bar.admin.ch.
- Technical questions or problems concerning the source code can be posted here on GitHub via the "Issues" interface.
