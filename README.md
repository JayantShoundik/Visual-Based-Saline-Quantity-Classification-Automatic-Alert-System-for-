ICU IV Fluid Monitoring & Automated Alert System using Machine Learning and IoT
📌 Overview

This project presents a Machine Learning–based intelligent monitoring system designed for real-time tracking of IV saline and glucose bottle levels in a hospital ICU setting.

In a typical ICU ward with multiple beds (e.g., 30 patients), continuous manual monitoring of IV fluid levels is time-consuming and prone to human delay. This system integrates computer vision and IoT-based monitoring to automatically detect fluid levels and trigger alerts when critical thresholds are reached.

The system classifies bottle states into predefined categories (50%, 30%, 20%, 10%, Empty) and sends automated notifications to the on-duty nurse for timely intervention.

🏥 Problem Statement

In hospital ICU environments:

Each patient may be connected to saline, glucose, or other IV fluids.

Manual supervision is required to prevent fluid depletion.

Delayed replacement can cause treatment interruptions or clinical risk.

This system aims to:

Automate IV bottle level detection

Reduce dependency on manual monitoring

Provide real-time alerts for critical fluid levels

⚙️ System Architecture

Image Acquisition (IoT Integration)
Cameras/sensors capture IV bottle images in real-time.

Machine Learning Classification
A trained ML model processes images and classifies fluid levels into:

sal_data_50

sal_data_empty

(Other defined threshold states such as 30%, 20%, 10%)

Alert Triggering Mechanism
When fluid levels reach predefined thresholds (e.g., 50%, 30%, 20%, 10%, or empty), an automated alert is sent to the mobile device of the nurse on duty.

🧠 Model Performance & Evaluation
🔍 Visual Inspection

Displayed 9 sample test images with:

True labels

Predicted labels

Correct predictions highlighted in green

Incorrect predictions highlighted in red

This provided immediate qualitative validation of system accuracy.

📊 Confusion Matrix Analysis
sal_data_50 (50% level)

Correctly classified: 159 / 160 images

Misclassified: 1 image

Demonstrates high precision and recall

sal_data_empty (Empty)

Correctly classified: 157 / 157 images

Achieved perfect recall for this category

sal_data_full

0 true samples in test set

Unable to evaluate performance for this class

Highlights need for balanced dataset expansion

🚨 Alert System Functionality

For all detected critical states (50% and empty during testing), the system successfully triggered "ALERT" messages.

Alerts are designed to notify the on-duty nurse via mobile device.

Ensures:

Timely IV replacement

Reduced manual supervision

Improved ICU workflow efficiency

📈 Key Findings

High classification accuracy for 50% and empty states.

Robust performance validated through confusion matrix evaluation.

Alert system functions reliably for critical thresholds.

Dataset imbalance (absence of full-state samples) identified as a limitation.

⚠️ Limitations

No sal_data_full samples in test dataset.

Model performance for full-state detection remains unvalidated.

Real-world deployment requires:

More diverse lighting conditions

Larger and balanced dataset

Hardware calibration for IoT integration

🔮 Future Improvements

Expand dataset to include all bottle states.

Implement class imbalance handling techniques.

Deploy real-time camera-based monitoring with edge inference.

Integrate hospital notification systems (SMS / app-based alerting).

Add predictive modeling for estimating remaining time before depletion.

🏆 Potential Impact

This system can:

Improve ICU efficiency

Reduce nursing workload

Prevent fluid depletion incidents

Enable scalable smart-hospital automation
