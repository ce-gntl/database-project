## Conceptual design

### Cimeta: the animal shelter of the University of Rome ‘’Tor Vergata’’

#### REQUIREMENTS COLLECTION AND ANALYSIS

We want to build a database for the management of the CIMETA animal shelter in order to collect data on the animal species present inside, the professional figures managing the animal shelter, the subdivision of the rooms, the researchers assigned and the research projects. Inside the animal shelter, the rooms (about 20\) are divided into: offices, laboratories, surgical room and rooms for the shelter. For the rooms, we want to represent the room number, the name of the room and a short description. In particular, for the shelter rooms (about 5\) we also want to obtain the maximum capacity and the animal species present.

For each person (about 50\) who has access to the animal shelter, we want to store the following information: name, surname, tax code, telephone number, email, date of birth and professional title. Each person will have a badge with a unique identification code. The staff is divided into two categories: technical- administrative area employees and researchers. For the technical-  
administrative staff (about 20\) we represent the position held and the room to which they refer. 

For the researchers (about 30\) we want to know the reference project and the reference body that can be internal if it comes from a department of the University of Tor Vergata or can be external if it comes from other national and international projects. Each researcher is associated with a research project. For the research project (about 5\) we want to represent the title of the project, the duration of the project, the approval date, the owner of the project and the veterinarian responsible for the project.

The animals (about 200\) can be divided into normal and GMO. For the animals we want to obtain an identification code, the species of the animal, the identifier of the strain, the name of the supplier, the project to which they are associated, the number of the room in which they are stabled and the treatments to which they are subjected.

#### DATA SPECIFICATIONS

Experimentation within the Animal Facility can only be permitted if the research project is approved. Researchers must send the necessary documentation to the responsible Veterinarian who will send it to the competent Authorities. After the experimental protocol is approved, a responsible Veterinarian is assigned to each research project. Each veterinarian can be assigned to multiple research projects. The experimental manual skills of the researchers will be checked by the Veterinarian in charge of the research project.

Access to the Animal Facility is only permitted to researchers identified within the research project. Each research project has a contact person for the research project. The contact person for the research project is required to send the Animal Facility Manager the names of the researchers/collaborators participating in the project. Each researcher will have an entry “badge” to the animal facility buildings which will be deactivated on the expiry date of the project. Each user must have adequate training to handle and/or use animals. If not, before accessing the experimentation, he/she is required to attend a specific training course.The animal facility provides each researcher with disposable material (disposable clothing, mask, cap and overshoes) to access the manipulation of biological derivatives and experimental procedures on animals. When entering the STA premises, researchers must record their entry time, name and telephone number; when leaving, the time must be reported in the appropriate register.

Each researcher can use the surgical, pre-surgical and laboratory rooms upon reservation.  
The animals are divided into GMO and healthy based on the ID of the strain that reports the species and any mutations. The animals to be entrusted to the Animal Facility must come from accredited farms and after verification of the state of health certified by a specific health monitoring report. Before proceeding with the purchase of the animals to be kept or used in the Animal Facility, researchers must ensure that the spaces for their maintenance are available at the facility. Colonies of normal or “GMO” animals will be entrusted to the animal facility staff for ordinary management and all other activities are the responsibility of the research group or individual researcher. The animals must be treated (except for experiments specifically authorized by the Ministry of Health) only in internal laboratories and only by researchers included in the research project. An animal can be reused later by another research project.

#### OPERATION SPECIFICATIONS

The operations foreseen on the database are the following:

##### 1\. Researchers.

(a) Registration of a new researcher.  
(b) Cancellation of the researcher based on the end of the project.  
(c) Modification of the data relating to a researcher  
(d) Deactivation of the researcher's badge at the end of the project.

##### 2\. Research project.

(a) Insertion of a new research project.  
(b) Change of the duration of the research project.  
(c) Updating of the information relating to an existing research project.

##### 3\. Technical-administrative staff.

(a) Registration of a new employee.  
(b) Cancellation of the employee.  
(c) Modification of the data relating to an employee.  
(d) Deactivation of the employee's badge.

##### 4\. Register.

(a) Registration of the entry and exit times for each researcher. .  
(b)Delete all entries and exits between two dates provided at the entrance.

##### 5.Rooms.

(a)Register a room reservation.  
(b)Delete a room reservation.

##### 6\. Animals.

(a)Register an animal.  
(b)Add and modify the research project to which it is currently associated.  
(c)Delete the animal if deceased.

##### 7.Other management procedures (basic)

(a)Given a badge, return the data relating to the researcher currently in its possession, indicating his/her personal data and the research project to which they are assigned.  
(b)Given the research project, extrapolate the data relating to the responsible veterinarian.  
(c)Given the research project, extrapolate the data relating to the animals currently assigned to the project.  
(d)Given the identification code of a researcher, extrapolate the number of entries of the same in a period of time.  
(e)Given a room number, see the reservations in a certain time range.