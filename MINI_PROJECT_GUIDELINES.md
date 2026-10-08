# Mini Project Guidelines: C Programming and Software Engineering

## 1. Objective

Design and implement a realistic engineering software solution using the C programming language and fundamental software engineering practices.

The mini project must demonstrate practical understanding of:

- Problem identification and requirement definition
- C programming
- Modular software design
- Coding standards and guidelines
- Data structures using C structures and enumerations
- Functions with clear arguments, return values and responsibilities
- Input validation and error handling
- File handling
- Unit testing using Google Test (gTest)
- Makefile-based build automation
- Git version control
- GitHub repository management
- Technical documentation

The final submission must be a complete software project that another developer can understand, build, run, test and extend.

The project must not be a collection of unrelated C programs. All modules must work together to solve one clearly defined problem.

---

## 2. Project Expectations

This is an individual mini project. You are expected to think like a software engineer, not only as a programmer.

You must:

1. Identify a meaningful engineering scenario.
2. Understand and define the problem.
3. Identify the expected users.
4. Define the project scope.
5. Write functional and non-functional requirements.
6. Design the software architecture and modules.
7. Define the required data structures and functions.
8. Implement the solution using modular C code.
9. Follow consistent coding standards.
10. Test important functions using gTest.
11. Automate building and testing using a Makefile.
12. Maintain the project using Git.
13. Publish the complete project on GitHub.
14. Share the GitHub repository link as the final submission.

Do not begin coding before completing the proposal and design.

---

## 3. Project Phases

The mini project has four phases:

1. Project Proposal
2. Detailed Software Design
3. Implementation and Testing
4. Documentation, GitHub Publication and Demonstration

---

# Phase 1: Project Proposal

## 4. Choose an Engineering Scenario

Select a realistic scenario from a domain such as:

- Automotive
- Manufacturing
- Healthcare
- Agriculture
- Energy
- Transportation
- Defence
- Education
- Laboratory management
- Inventory and warehouse management
- Environmental monitoring
- Utility management
- Equipment maintenance

Possible examples include:

- Vehicle service record management
- Factory equipment maintenance tracking
- Energy consumption analysis
- Water usage record management
- Warehouse inventory management
- Vehicle fleet record management
- Parking management
- Hospital patient record management
- Production record analysis
- Equipment fault record management
- Traffic violation record management
- Laboratory asset management
- Fuel consumption analysis
- Battery health record analysis
- Machine inspection record management

These are only examples. You are encouraged to identify your own engineering scenario.

The selected scenario should involve several of the following operations:

- Data entry
- Data validation
- Data storage
- Data retrieval
- Data modification
- Searching
- Sorting or filtering
- Calculations
- Decision-making
- Status determination
- Report generation
- File handling

The following are not sufficient as mini projects:

- Basic calculator
- Number conversion program
- Simple menu demonstration
- A single C program without modules
- A collection of unrelated functions
- A copied project without design justification

---

## 5. Project Proposal Requirements

The project proposal must contain the following sections.

### 5.1 Project Title

Provide a clear and meaningful project title that reflects the problem being solved.

### 5.2 Student Information

Provide:

- Student name
- Roll number
- Division or batch
- Project title
- GitHub repository link

### 5.3 Engineering Scenario

Explain:

- The selected domain
- The real-world situation
- Where the problem occurs
- Who faces the problem
- Why a software solution is useful

### 5.4 Problem Statement

Clearly state:

- The existing problem
- Limitations of the current approach
- Information that needs to be managed
- Expected result from the proposed solution

### 5.5 Proposed Solution

Describe the software solution at a high level.

Explain:

- What the application will do
- How it will help the user
- What major operations it will support
- What output or reports it will generate

### 5.6 Target Users

Identify the expected users of the system and briefly explain how each user will use it.

### 5.7 Project Scope

Define the project boundary using two lists:

- In-scope features
- Out-of-scope features

The scope must be realistic for the available project duration.

### 5.8 Functional Requirements

Specify what the system must do.

Each functional requirement must have a unique identifier such as FR-01, FR-02 and FR-03.

Example requirement format:

- FR-01: The system shall add a new equipment record.
- FR-02: The system shall validate the equipment identifier.
- FR-03: The system shall search for equipment using its identifier.

Requirements must describe behaviour, not implementation details.

### 5.9 Non-Functional Requirements

Specify expected software quality, including:

- Code readability
- Modular design
- Input validation
- Error handling
- Warning-free compilation
- Automated unit testing
- Build automation
- Documentation
- Version control

### 5.10 Initial Modules

Identify the major modules expected in the solution and state the responsibility of each module.

### 5.11 Initial Architecture Diagram

Create a high-level block diagram showing:

- User
- Application interface
- Application modules
- Data processing
- File storage
- Reports or outputs

### 5.12 High-Level Workflow

Show how a user will interact with the application from start to exit.

### 5.13 Planned C Concepts

List the C concepts planned for the project and explain why they are needed.

Possible concepts include:

- Functions
- Structures
- Enumerations
- Arrays
- Strings
- Pointers
- Constants
- File handling
- Dynamic memory allocation, if justified
- Error or status codes

---

# Phase 2: Detailed Software Design

## 6. Software Architecture

Explain how the software is organised.

A recommended architecture may contain:

- User interface layer
- Application or business-logic layer
- Validation layer
- Data-management layer
- File-storage layer
- Report-generation layer

The design must match the selected problem. Do not create unnecessary layers or modules only to increase the file count.

---

## 7. Module Design

For each module, specify:

- Module name
- Source filename
- Header filename
- Purpose
- Public functions
- Data used by the module
- Other modules on which it depends
- Errors or status codes returned

The complete application must not be implemented in main.c.

The main.c file should mainly:

- Initialise the application
- Load existing data
- Display the main menu
- Call functions from other modules
- Control the high-level workflow
- Save data when required
- Perform final cleanup

---

## 8. Data Design

Define the data required by the project.

The data design should include:

- Structures
- Enumerations
- Constants
- Array sizes
- String-size limits
- Valid ranges
- Relationships between records

Create a data dictionary containing:

- Data item name
- C data type
- Valid range or size
- Description
- Validation rule

Use named constants instead of unexplained numeric or string values.

---

## 9. Function Design

Document every important function before implementation.

For each function, specify:

- Function name
- Declaration or prototype
- Purpose
- Input parameters
- Output parameters
- Return type
- Return values
- Preconditions
- Postconditions
- Errors handled
- Module in which the function is implemented

Functions should have one clear responsibility and should be independently testable wherever possible.

---

## 10. Input-Validation Plan

Identify all user and file inputs that require validation.

The plan should define rules for:

- Integer values
- Floating-point values
- Text fields
- Identifiers
- Enumerated choices
- Empty input
- Duplicate records
- Minimum and maximum values
- Maximum string lengths
- Unsupported menu choices
- Invalid file data

The program must handle invalid input without crashing or entering an uncontrolled state.

---

## 11. File-Handling Plan

Explain:

- Files used by the application
- Purpose of each file
- Text or binary format
- Data stored in each file
- When files are created
- When files are read
- When files are updated
- How file errors are handled

Use appropriate C file-handling functions according to the design.

Possible functions include:

- fopen()
- fclose()
- fgets()
- fputs()
- fscanf()
- fprintf()
- fread()
- fwrite()

All file operations must be checked for success or failure.

---

## 12. Error-Handling Strategy

Define how the software will report and manage errors.

The design should consider:

- Invalid arguments
- Null pointers
- Invalid indexes
- Duplicate records
- Missing records
- Empty data collections
- Maximum storage capacity
- File-open failure
- File read or write failure
- Invalid file content
- Memory-allocation failure, if applicable

Use consistent status codes or enumerations where appropriate.

Do not ignore function return values.

---

## 13. Application Flow

Create an application flowchart showing:

- Application start
- Initialisation
- Loading stored data
- Displaying the menu
- Receiving a user choice
- Validating input
- Calling the appropriate module
- Displaying success or error information
- Saving updated data
- Application exit

Create separate flowcharts for complex operations where required.

---

## 14. Unit-Test Plan

Identify the important functions that will be tested.

For each function, define:

- Positive test cases
- Negative test cases
- Boundary test cases
- Input values or conditions
- Expected result

Suitable functions for unit testing include:

- Validation functions
- Search functions
- Calculation functions
- Sorting and filtering functions
- Status-determination functions
- Record insertion functions
- Record deletion functions
- Report-calculation functions

Menu display and simple printing functions should not be the main focus of unit testing.

---

# Phase 3: Implementation and Testing

## 15. C Implementation Requirements

The implementation must include:

- A modular, multi-file C project
- main.c as the application entry point
- At least three meaningful implementation modules in addition to main.c
- Corresponding header files
- At least one meaningful structure
- Enumerations where appropriate
- Constants instead of magic numbers
- Functions with clear parameters and return values
- Input validation
- Error handling
- File handling
- Meaningful calculations or decision-making
- Report generation or processed output

The number of modules must be based on project needs. Empty or unnecessary modules will not receive additional credit.

---

## 16. Coding Standards and Guidelines

### 16.1 Naming

Use meaningful and consistent names for:

- Files
- Variables
- Functions
- Structures
- Enumerations
- Constants

Function names should normally describe actions, such as:

- addRecord()
- findRecordById()
- calculateAverageConsumption()
- saveRecordsToFile()

Constants should use uppercase names.

### 16.2 Formatting

Follow these rules:

- Use four spaces for indentation.
- Do not mix tabs and spaces.
- Use consistent brace placement.
- Keep one statement per line.
- Use spaces around operators.
- Use blank lines to separate logical sections.
- Maintain the same format in all source files.

### 16.3 Function Quality

Each function should:

- Perform one clear responsibility
- Check pointer arguments when applicable
- Validate relevant inputs
- Return a meaningful result or status
- Avoid unnecessary side effects
- Be small enough to understand and test

### 16.4 Header Files

Header files should contain:

- Header guards
- Required public type definitions
- Public constants, where appropriate
- Public function declarations
- Only the required includes

Do not place normal function implementations in header files.

### 16.5 Comments

Comments should explain:

- Purpose
- Assumptions
- Function parameters
- Return values
- Non-obvious logic

Do not write comments that merely repeat the code.

### 16.6 Practices to Avoid

Do not:

- Place the complete application in main.c
- Ignore compiler warnings
- Ignore function return values
- Use unexplained magic numbers
- Use unnecessary global variables
- Duplicate logic
- Keep unused variables or functions
- Submit commented-out unused code
- Use unsafe input functions
- Hard-code machine-specific absolute paths
- Copy code without understanding it

---

## 17. Compiler Requirements

Use strict compiler warnings.

Recommended flags:

    -Wall -Wextra -Wpedantic

The final project must compile without warnings.

---

## 18. Unit Testing with Google Test

The application must include automated unit tests using Google Test.

The main application must be written in C. Test files may be written in C++ to use gTest.

C headers used by the C++ test files must provide C linkage where required.

### Minimum Testing Requirements

The project must include:

- Tests for at least three important functions
- At least ten meaningful test cases
- Positive tests
- Negative tests
- Boundary-value tests
- Independent and repeatable tests
- Clear test-suite and test-case names
- Test execution using make test

Repeated tests of the same behaviour will not be considered separate meaningful test cases.

Each test must:

- Test one clear behaviour
- Define an expected result
- Avoid dependence on test execution order
- Avoid unnecessary user input
- Clean up temporary test data
- Fail when the corresponding implementation is incorrect

---

## 19. Makefile Requirements

The project must use a Makefile.

The Makefile must support:

    make all
    make run
    make test
    make clean

The Makefile should:

- Use variables for compilers and flags
- Compile source files separately
- Generate object files
- Link the application
- Build the gTest executable
- Include the required header directories
- Rebuild only when dependencies change
- Remove generated files through make clean

A user should not need to compile individual files manually before using the Makefile.

---

## 20. Recommended Repository Structure

    project-name/
    |
    |-- src/
    |   |-- main.c
    |   |-- record.c
    |   |-- validation.c
    |   |-- file_handler.c
    |   `-- report.c
    |
    |-- include/
    |   |-- record.h
    |   |-- validation.h
    |   |-- file_handler.h
    |   `-- report.h
    |
    |-- tests/
    |   |-- test_record.cpp
    |   |-- test_validation.cpp
    |   `-- test_report.cpp
    |
    |-- data/
    |   `-- sample_data.txt
    |
    |-- docs/
    |   |-- project_proposal.md
    |   |-- detailed_design.md
    |   `-- architecture.png
    |
    |-- Makefile
    |-- README.md
    |-- .gitignore
    `-- LICENSE

Adapt file and module names to your project.

---

# Phase 4: GitHub Publication and Demonstration

## 21. Individual Project and Academic Integrity

This mini project must be completed individually.

You may discuss general concepts and approaches with classmates, but the following work must be your own:

- Problem definition
- Requirements
- Software design
- Source code
- Unit tests
- Makefile
- Documentation
- Git commit history
- Demonstration and explanation

Direct copying of another student's design, source code, tests or documentation is not permitted. Any external reference used must be understood and acknowledged appropriately.

You must be prepared to explain, modify and test any part of your submission during evaluation.

---

## 22. Git Requirements

Use Git throughout development.

The project history should show gradual development through multiple meaningful commits.

Good commit-message examples:

- Create initial project structure
- Add equipment data model
- Implement input validation
- Implement record search
- Add file-storage module
- Add validation unit tests
- Update Makefile with test target
- Document build and run steps
- Fix duplicate-record handling

Avoid unclear messages such as:

- update
- changes
- final
- latest
- working code

---

## 23. GitHub Repository Requirements

Create a GitHub repository with a meaningful name.

The repository must contain:

- C source files
- Header files
- gTest files
- Makefile
- README.md
- Project proposal
- Detailed design
- Architecture diagram
- Required sample data
- .gitignore

Do not commit:

- Object files
- Generated executables
- Build-directory contents
- Temporary editor files
- Core dumps
- Unnecessary IDE configuration

Before submission, clone the repository into a new directory and verify that:

1. The README instructions are complete.
2. make all works.
3. make test works.
4. make run works.
5. All required files are present.
6. Generated files are not tracked.

---

## 24. README Requirements

The root of the repository must contain README.md with:

- Project title
- Engineering domain
- Problem statement
- Proposed solution
- Features
- Functional requirements summary
- Software architecture
- Module descriptions
- Folder structure
- C concepts used
- Coding standards followed
- Prerequisites
- Build instructions
- Run instructions
- Test instructions
- Sample input
- Sample output
- Unit-testing summary
- Error-handling summary
- Student information
- Known limitations
- Future enhancements
- GitHub repository link

The README must allow another developer to build and run the project without additional verbal instructions.

---

## 25. Project Deliverables

Submit the following:

### 25.1 Project Proposal

Include:

- Project title
- Student information
- Engineering scenario
- Problem statement
- Proposed solution
- Target users
- Project scope
- Functional requirements
- Non-functional requirements
- Initial modules
- Initial architecture
- High-level workflow
- Planned C concepts

### 25.2 Detailed Design

Include:

- Software architecture
- Module design
- Module responsibilities
- Data design
- Function specifications
- Input-validation plan
- File-handling plan
- Error-handling strategy
- Application flowchart
- Unit-test plan

### 25.3 Source Code

Include:

- Modular C source files
- Header files
- Input validation
- Error handling
- File handling
- Meaningful processing
- No unused code or variables
- Warning-free build

### 25.4 Unit Tests

Include:

- gTest source files
- Positive test cases
- Negative test cases
- Boundary test cases
- Repeatable tests
- Successful execution through make test

### 25.5 Makefile

Must support:

    make all
    make run
    make test
    make clean

### 25.6 README

Provide complete build, run, test and project documentation.

### 25.7 GitHub Repository

Share the complete and accessible GitHub repository link.

### 25.8 Demonstration

Demonstrate:

1. Engineering problem
2. Functional requirements
3. Software architecture
4. Repository structure
5. Project build
6. Application execution
7. Important features
8. Invalid-input handling
9. Unit-test execution
10. Makefile targets
11. Commit history
12. GitHub repository

### 25.9 Reflection

Briefly explain:

- What worked well
- Challenges faced
- How challenges were resolved
- What you learned
- Future improvements

---

## 26. Submission Checklist

### Proposal and Design

- [ ] Engineering scenario is realistic.
- [ ] Problem statement is clear.
- [ ] Target users are identified.
- [ ] Scope is defined.
- [ ] Functional requirements are documented.
- [ ] Non-functional requirements are documented.
- [ ] Architecture diagram is included.
- [ ] Modules are identified.
- [ ] Data structures are designed.
- [ ] Major functions are specified.
- [ ] Error-handling strategy is defined.
- [ ] Unit-test plan is prepared.

### Implementation

- [ ] Multiple C source files are used.
- [ ] Header files are provided.
- [ ] main.c contains only high-level control.
- [ ] Structures are used meaningfully.
- [ ] Functions have clear parameters and return values.
- [ ] Input is validated.
- [ ] File operations are checked.
- [ ] Errors are handled.
- [ ] Coding standards are followed.
- [ ] Code compiles without warnings.
- [ ] No unused code is present.

### Unit Testing

- [ ] gTest is used.
- [ ] At least three important functions are tested.
- [ ] At least ten meaningful tests are included.
- [ ] Positive tests are included.
- [ ] Negative tests are included.
- [ ] Boundary tests are included.
- [ ] Tests are repeatable.
- [ ] make test works.
- [ ] All tests pass.

### Makefile

- [ ] make all works.
- [ ] make run works.
- [ ] make test works.
- [ ] make clean works.

### Git and GitHub

- [ ] Git was used throughout development.
- [ ] Multiple meaningful commits are present.
- [ ] .gitignore is configured.
- [ ] Generated files are not committed.
- [ ] The repository contains the complete project.
- [ ] The repository was cloned and independently verified.
- [ ] The correct GitHub link is submitted.

### Documentation

- [ ] README explains the problem and solution.
- [ ] Architecture is documented.
- [ ] Folder structure is documented.
- [ ] Build instructions are correct.
- [ ] Run instructions are correct.
- [ ] Test instructions are correct.
- [ ] Sample output is included.
- [ ] Limitations are documented.
- [ ] Future enhancements are documented.

---

## 27. Expected Engineering Mindset

Follow this development process:

    Understand the problem
              |
              v
    Define requirements
              |
              v
    Design the software
              |
              v
    Implement modular C code
              |
              v
    Follow coding standards
              |
              v
    Build using a Makefile
              |
              v
    Test using Google Test
              |
              v
    Document the project
              |
              v
    Publish and verify on GitHub

The goal is to deliver a software project that another developer can understand, build, run, test, review, maintain and extend.
