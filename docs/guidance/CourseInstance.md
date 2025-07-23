# Guidance for using CourseInstance

The [CourseInstance](http://schema.org/CourseInstance) profile fits into the schema.org hierarchy as follows:

[Thing](http://schema.org/Thing) > [Event](http://schema.org/Event) > [CourseInstance](http://schema.org/CourseInstance)

## Example using CourseInstance
A specific instance of a graduate-level course instance, offered in a blended format, focusing on the foundational concepts and modern theories of quantum gravity, provided by a leading university.

### JSON-LD code

```json
{
    "@context": "https://schema.org",
    "@type": "CourseInstance",
    "http://purl.org/dc/terms/conformsTo": {
        "@id": "https://bioschemas.org/profiles/Course/1.0-RELEASE",
        "@type": "CreativeWork"
    },
    "name": "Introduction to Quantum Gravity - Fall 2024",
    "description": "An intensive graduate-level course instance for the Fall 2024 semester, exploring the current theoretical frameworks and challenges in unifying quantum mechanics with general relativity, including string theory, loop quantum gravity, and emergent gravity concepts. This course will be delivered in a blended format, combining online lectures with in-person discussion sessions.",
    "courseMode": "Blended",
    "startDate": "2024-09-02",
    "endDate": "2024-12-13",
    "course": {
        "@type": "Course",
        "name": "Introduction to Quantum Gravity",
        "description": "This is the general curriculum for the Quantum Gravity course, covering advanced topics in theoretical physics.",
        "coursePrerequisites": "Graduate-level knowledge of Quantum Mechanics and General Relativity.",
        "educationalCredentialAwarded": "Certificate of Completion"
    },
    "location": {
        "@type": "VirtualLocation",
        "url": "https://university.example.edu/quantum-gravity-virtual-classroom",
        "name": "Online Quantum Gravity Classroom"
    },
    "provider": {
        "@type": "Organization",
        "name": "University of Cambridge",
        "department": {
            "@type": "Organization",
            "name": "Department of Applied Mathematics and Theoretical Physics (DAMTP)"
        },
        "url": "https://www.damtp.cam.ac.uk/"
    },
    "instructor": {
        "@type": "Person",
        "name": "Prof. Alice Quantum",
        "url": "https://university.example.edu/prof-quantum-profile",
        "affiliation": {
            "@type": "Organization",
            "name": "University of Cambridge, DAMTP"
        }
    },
    "audience": {
        "@type": "EducationalAudience",
        "audienceType": "Graduate students in Physics",
        "educationalLevel": "Graduate"
    },
    "inLanguage": "en-US",
    "offers": {
        "@type": "Offer",
        "price": "1500",
        "priceCurrency": "GBP",
        "url": "https://university.example.edu/quantum-gravity-enrollment-fall2024",
        "availability": "http://schema.org/InStock",
        "validFrom": "2024-06-01",
        "validThrough": "2024-08-15",
        "category": "Course Fee"
    },
    "maximumAttendeeCapacity": 100,
    "eventStatus": "http://schema.org/EventScheduled"
}
```

### Diagram

```mermaid
graph LR
CourseInstance_QG_Fall2024["CourseInstance: Introduction to Quantum Gravity - Fall 2024"]
Course_QG["Course: Introduction to Quantum Gravity"]
EducationalAudience_GradPhysics["EducationalAudience: Graduate students in Physics"]
Organization_Cambridge["Organization: University of Cambridge"]
Organization_DAMTP["Organization: Department of Applied Mathematics and Theoretical Physics (DAMTP)"]
Person_ProfQuantum["Person: Prof. Alice Quantum"]
VirtualLocation_OnlineRoom["VirtualLocation: Online Quantum Gravity Classroom"]
Offer_Enrollment["Offer: Enrollment"]
Text_Blended["Text: Blended"]
Text_English["Text: en-US"]
EventStatus_Scheduled["EventStatus: EventScheduled"]

CourseInstance_QG_Fall2024 -->|course| Course_QG
CourseInstance_QG_Fall2024 -->|audience| EducationalAudience_GradPhysics
CourseInstance_QG_Fall2024 -->|provider| Organization_Cambridge
Organization_Cambridge -->|department| Organization_DAMTP
CourseInstance_QG_Fall2024 -->|instructor| Person_ProfQuantum
CourseInstance_QG_Fall2024 -->|location| VirtualLocation_OnlineRoom
CourseInstance_QG_Fall2024 -->|courseMode| Text_Blended
CourseInstance_QG_Fall2024 -->|inLanguage| Text_English
CourseInstance_QG_Fall2024 -->|offers| Offer_Enrollment
CourseInstance_QG_Fall2024 -->|eventStatus| EventStatus_Scheduled
```