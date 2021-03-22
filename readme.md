[Deutsch](readme_de.md) :point_left:

# cmi-viaduc
- **[cmi-viaduc](https://github.com/SwissFederalArchives/cmi-viaduc)** :triangular_flag_on_post:
   - [cmi-viaduc-web-core](https://github.com/SwissFederalArchives/cmi-viaduc-web-core)
   - [cmi-viaduc-web-frontend](https://github.com/SwissFederalArchives/cmi-viaduc-web-frontend)
   - [cmi-viaduc-web-management](https://github.com/SwissFederalArchives/cmi-viaduc-web-management)
   - [cmi-viaduc-backend](https://github.com/SwissFederalArchives/cmi-viaduc-backend)

# Introduction
Viaduc was the project name during development of the online access of the Swiss Federal Archives (webOZ).

The online access of the SFA can be described as a digital reading room, since it can handle a large part of the archive's tasks on it's digital platform. 
The following features are worth highlighting:
- Search in public metadata and primary data.
- Search in protected metadata and primary data for authorized users.
- Differentiated authorization concept for accessing metadata and primary data based on the logged-in user.
- Downloading primary data (DIP) as a working copy.
- Ordering of archive records as digital copies. (The archive records are digitized in a timely manner and made accessible to the user.)
- Preparation of the working copy includes
  - OCR recognition of scans
  - Format conversion from archive to user formats
- Storage of public working copies in a cache
- Issuing requests for insight to protected files
- Temporary access of documents to authorized persons upon request
- Government offices have access to their own documents
- Internal web application to manage orders, insight requests, administrative access and settings.

In order for the archive community to benefit from the investment, knowledge and solutions to various problems, the SFA has decided to make the source code available as open source.

# Overview
The complete solution of the online access of the Federal Archives (webOZ) includes 4 code repositories. 

The repository [cmi-viaduc-web-core](https://github.com/SwissFederalArchives/cmi-viaduc-web-core) is an Angular library. 
This library is used by the other two applications Public Access  ([cmi-viaduc-web-frontend](https://github.com/SwissFederalArchives/cmi-viaduc-web-frontend)) and Internal Management ([cmi-viaduc-web-management](https://github.com/SwissFederalArchives/cmi-viaduc-web-management)) as a common code base and component library. 
The frontend applications are hosted in an `ASP.NET` container (see backend repository [cmi-viaduc-backend](https://github.com/SwissFederalArchives/cmi-viaduc-backend)) and communicate with the system via web API.

![The Big-Picture](docs/imgs/context.svg)

# Authors
- [CM Informatik AG](https://cmiag.ch)
- [Evelix GmbH](https://evelix.ch)

# License
All repositories are licensed under the same license:
GNU Affero General Public License (AGPLv3), see [LICENSE](LICENSE.TXT).

# Project status
The initial development project is finished, currently the webOZ is in the maintenance/continuation phase.
It is planned to make selective developments, corrections and improvements every year and to publish them here.

# Contribute
This is a copy which will be updated regularly - therefore contributions via pull requests are not possible. However, independent copies (forks) are possible under consideration of the AGPLV3 license.

# Contact
- For general questions (and technical support), please contact the Swiss Federal Archives by e-mail at bundesarchiv@bar.admin.ch.
- Technical questions or problems concerning the source code can be posted on GitHub via "Issue".
