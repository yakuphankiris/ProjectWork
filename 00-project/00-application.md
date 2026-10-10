---
name: Yakuphan Kiris
neptun: JDCZNC
id: 2026_SD_4
---
# Receipt-based Shared Expense Allocation Application

## My interpretation of the brief
The project is a mobile and web application for recording, allocating, and settling shared expenses within a group. A user photographs a receipt, and OCR combined with an LLM or a multimodal model suggests an editable list of items, quantities, and amounts while preserving links to the relevant image regions. Users review the extracted data, select the payer and participants, and divide expenses using equal, percentage-based, or fixed-amount rules. The application must handle rounding, discounts, balances, approvals, edit history, settlements, duplicate warnings, and exportable summaries reliably. Its AI-supported extraction must remain reviewable and correctable, while the financial calculations must be deterministic and independently tested.

## Why I am a good fit for this project
During my internship, I worked with another intern to develop a driver-tracking system for mobile devices using Flutter and Dart. This gave me practical experience in collaborative mobile development, designing user flows, handling application data, and turning real operational requirements into a working application. Since this project also requires a mobile interface and a clear workflow for capturing, reviewing, and approving data, that experience provides me with a relevant starting point.

I am very enthusiastic about this project because it combines mobile and web development, persistent data, financial calculation rules, image processing, and artificial intelligence. I believe that completing it would help me strengthen my existing Flutter and Dart skills while developing myself in several new areas. I do not yet have practical experience with LLM integration, but I am motivated to learn how to use an LLM or a multimodal AI service responsibly in a real application. This is one of the main reasons why I would like to take on the project.

## Relevant experience and background
My internship project gave me experience with Flutter and Dart as well as working together with another developer on a mobile application. Developing a driver-tracking system taught me to think about mobile usability, data flow, application structure, and the reliability of information presented to users. I also have experience with C#, the .NET Framework, Microsoft SQL Server, and database-backed applications, which would help me design the server-side and persistence parts of this project.

Although OCR and LLM integration would be new areas for me, I am interested in learning them through a structured process. I would begin with small experiments, evaluate the extracted data against manually checked receipts, and keep the AI component separate from the deterministic expense-allocation logic. This would allow me to build on my current experience while gaining practical knowledge of AI integration and evaluation.

## Proposed approach
I would use Flutter and Dart for the mobile application and evaluate Flutter Web for the browser-based expense view. I would use a server-side API and persistent relational storage for groups, members, receipts, expenses, items, discounts, allocation rules, approvals, edit history, settlements, and exported summaries. Monetary values would be stored either as exact decimals or in the smallest currency unit to avoid floating-point rounding errors.

For receipt processing, the mobile application would capture and upload an image to the server. I would first establish a basic OCR baseline and then compare it with structured processing using an LLM or a multimodal model. The extraction result would include suggested item names, quantities, amounts, confidence or uncertainty information, and references to the relevant receipt-image regions. Missing or uncertain fields would be highlighted for manual review, and users would always be able to correct the suggestions. AI failure or temporary unavailability would not remove existing data or prevent manual entry.

The allocation engine would be implemented independently of the AI component. It would support equal, percentage-based, and fixed-amount splits and would verify amount conservation, rounding remainders, discount allocation, and agreement with the receipt total. Group balances would be updated only after approval. Approval and settlement operations would use safe database transactions, and the system would preserve edit history, handle later corrections according to documented rules, warn about likely duplicate uploads, and prevent repeated approval from changing balances more than once.

I would evaluate basic OCR and structured AI processing on manually checked samples grouped by receipt layout. The comparison would measure item-name and amount recognition, required correction effort, and total entry time. Allocation, discounts, refunds, rounding, concurrent edits, and repeated approval would be tested separately with cases whose correct results are known in advance.

## Initial plan
1. Define the supported receipt types, user workflow, data model, allocation rules, refund handling, and the effect of later edits on settled balances.
2. Write the specification and design the architecture so that application, persistence, financial calculation, and AI integration logic remain separate.
3. Implement persistent management of groups, members, receipts, expenses, items, discounts, allocation rules, approvals, edit history, and manual settlements.
4. Build the Flutter mobile camera and review workflow together with the web-based expense view.
5. Implement and test equal, percentage-based, and fixed-amount allocation, including rounding, discounts, total verification, and balance updates after approval.
6. Implement a basic OCR pipeline, followed by structured LLM or multimodal processing with image-region references, uncertainty handling, and full manual correction.
7. Compare OCR and AI-assisted extraction on manually verified receipt samples, measuring recognition quality, correction effort, and entry time for different layouts.
8. Test duplicate detection, amount conservation, concurrent edits, repeated approval, AI-service failure, exports, and the complete user workflow.

## Additional information
I plan to maintain the source code in a Git repository with setup instructions, sample data, and a reproducible evaluation procedure. AI service credentials would remain on the server and would not be committed to the repository. Personal or production receipt data would not be used in the repository or evaluation dataset. I would start with one currency as required and focus first on delivering a reliable, testable core application before considering optional features.

For me, this project would be an opportunity to apply my previous mobile-development experience to a useful real-world problem and to improve my skills in web development, backend design, testing, OCR, and LLM integration. I am especially interested in learning how AI-assisted features can be incorporated without sacrificing correctness, transparency, or user control.
