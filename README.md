# Real-Time-3D-AR-with-Camera-Calibration-Pose-Estimation

## **Project Overview**
This project showcases a sophisticated 3D Augmented Reality (AR) system implemented in C++ using OpenCV. Designed for real-time applications, this AR system performs camera calibration, feature detection, and pose estimation to overlay virtual 3D objects onto a live video stream. It combines classic computer vision techniques with modern AR capabilities, providing an accurate projection of virtual objects in a real-world context, making it highly applicable to AR-based applications in fields like robotics, computer vision, and interactive media.

## **Technical Approach**

### 1. **Camera Calibration**
   - **Process**: This calibration uses predefined checkerboard and circle grid patterns to detect feature points, which are essential for calculating the intrinsic camera parameters. The project employs OpenCV’s `calibrateCamera` function to determine the camera matrix and distortion coefficients, enabling accurate 3D-to-2D point mapping.
   - **Result**: The computed reprojection error provides insight into calibration accuracy, with lower values indicating better alignment between the projected and actual feature points, resulting in a more realistic AR overlay.

### 2. **Pose Estimation and 3D Projection**
   - **Pose Estimation Using `solvePnP`**: The project relies on `solvePnP` to calculate rotation and translation vectors. These vectors are essential for determining the camera's viewpoint and for placing virtual objects accurately in relation to the real-world scene.
   - **3D Object Projection**: Using the camera’s position and orientation, the system projects 3D objects onto the target, aligning them with the physical environment in real-time. This projection dynamically updates as the camera or target moves, enhancing interactivity.

### 3. **Augmented Reality (AR) Overlay**
   - **Perspective Transformation for Image Replacement**: In addition to 3D objects, the project can replace a detected target with an image overlay using a custom transformation matrix. By computing a homography based on matched points, the system seamlessly maps the overlay onto the target.
   - **Virtual Axis and Object Drawing**: Displays 3D axes and geometric shapes (cube, pyramid, cylinder) directly on the detected target, simulating a real-world AR experience. Each axis and object aligns with the calculated pose, maintaining accuracy and realism.

## **Technical Skills and Knowledge Demonstrated**

### **Computer Vision & Image Processing**
   - **Expertise in Feature Extraction**: Demonstrates advanced knowledge in feature detection methods (Harris, Shi-Tomasi, chessboard, circle grid) for extracting distinct points of interest. These techniques ensure reliable feature tracking and provide a foundation for accurate calibration and pose estimation.
   - **Real-Time Video Processing and AR Rendering**: Proficient in handling live video streams, performing transformations, and projecting 3D content. This project exhibits an understanding of camera calibration and feature tracking as foundational elements for robust AR applications.

### **C++ Programming and OpenCV**
   - **Efficient Memory and Data Handling**: Utilizes C++ Standard Template Library (STL) containers like `vector` and `map` for efficient data handling in real-time scenarios. OpenCV functions are extensively used to manage image and matrix data, a core requirement for real-time AR.
   - **Modular, Well-Documented Codebase**: The project is organized into reusable, modular functions with detailed comments, enabling easy maintenance and future expansions.

### **Augmented Reality and 3D Transformations**
   - **3D Geometry and Transformations**: Demonstrates practical knowledge of 3D geometry, particularly in transforming and projecting 3D coordinates onto a 2D image plane. This is critical for accurately rendering 3D objects in relation to a real-world target.
   - **Depth Understanding of Camera Models**: Proficient in working with the camera pinhole model, distortion coefficients, and pose estimation, which are essential for AR applications requiring precise spatial awareness and object placement.

### **Data Persistence and Serialization**
   - **CSV-based Data Management**: Demonstrates familiarity with data persistence by saving and loading calibration data. This approach minimizes the need for repeated calibration, significantly enhancing user experience in practical applications.

---

## **Project Highlights**
This AR system leverages complex computer vision techniques to bridge the virtual and real worlds. By combining calibration, pose estimation, feature tracking, and real-time rendering, the project achieves high accuracy in AR content placement. The project’s emphasis on camera calibration, robust feature detection, and modular design underscores its versatility for AR applications across various industries.


