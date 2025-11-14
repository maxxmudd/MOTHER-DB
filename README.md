# MOTHER-DB
Python, Flask, JavaScript, HTML, Git - Coded 2024-2025. This repository describes my work done for the MOTHER-DB project.

[MOTHER-DB](https://mother-db.org/)

From August 2024 to December 2025, I have been a contributor for the multispecies ovarian tissue histology electronic repository (MOTHER). MOTHER is a searchable database of ovary tissue histology slides with associated specimen metadata. The tool is designed to maintain data provenance and provide a resource for researchers to advance future discoveries in reproductive biology.

My initial tasks were to develop input validation mechanisms for the ezEML+MOTHER tool, which is a fork of ezEML, a web application that streamlines the creation of metadata for ovary tissue specimens. MOTHER's extension of this tool adds additional data categories, including donor and immunohistochemistry information. I built upon the existing Flask-based forms in the tool, adding customized input validation mechanisms and updating form features to ensure invalid submissions do not reach MOTHER's curation stage, the backend system that processes metadata submissions to the MOTHER database. 

The result of this work removed the need for staff to oversee submissions and manually and inform users if there are mistakes in their metadata. The tool now produces automatic responses through error messages, preventing users from proceeding until their entries adhere to the form requirements. These mechanisms serve as the primary layer or protection from invalid data reaching the MOTHER database.

Regarding this work, I presented posters at the Arizona-Nevada Academy of Sciences (ANAS) as well as the New College Undergraduate Inquiry and Research Experiences (NCUIRE) Symposium, describing the input validation mechanisms and their importance in maintaining accurate and reliable data:

[Proceedings of the Arizona-Nevada Academy of Science, Volume 57 (2025)](https://repository.arizona.edu/bitstream/handle/10150/677000/2025_ANVAS.pdf)

(MOTHER dissemination page link coming soon)

Towards the end of my research, I focused mainly on the backend curation process, where I produced comprehensive unit tests using the Pytest framework. The curation process takes XML documents produced by the ezEML+MOTHER tool, and processes the fields to create entries in the MOTHER database. With the complex combination of form selections and entries that can take place for an ovary specimen, all possible selections and outcomes must be tested against the system's backend file validation checks to ensure entries do not violate the requirements put in place by MOTHER. The comprehensive unit tests include checks for all possible form field selections and combinations. Tests either produce an error when expected, or do not error for valid submissions. These checks need to take place prior to curation, and will halt the curation process prior to producing a database entry.

The result of this work has provided a secondary layer of protection for the MOTHER database, ensuring that all functioning components of the backend system are working properly for the curation stage, and that invalid XML documents do not get processed into the database.

All contributions to this project are tracked in my Activity log. For more information, please contact me.
