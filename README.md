# File-Encryption-and-Decryption-using-DES-Algorithm
This Java project focuses on implementing a secure file encryption and decryption system using the Data Encryption Standard (DES) algorithm. The system ensures the confidentiality of sensitive data through robust cryptographic techniques.

Key Features:

 DES Encryption and Decryption: Utilizes the Java Cipher class to perform encryption and decryption operations using the DES algorithm.
    Key Generation: Implements key generation using the KeyGenerator class for enhanced security.
    Initialization Vector (IV): Enhances security by employing an initialization vector (IV) in Cipher Block Chaining (CBC) mode.
    File Handling: Provides methods for encrypting and decrypting files of various sizes, ensuring smooth handling of input and output streams.
    Exception Handling: Incorporates comprehensive exception handling to address potential issues during cryptographic operations and file manipulation.
    User Interface: Enables users to specify file paths for input, encrypted output, and decrypted output.

Certainly! Here's the algorithm for the provided Java code for file encryption and decryption using the DES algorithm:

### Algorithm:

#### Encryption Algorithm:

1. **Initialize Parameters:**
   - Set the path of the file to be encrypted (`textFile`).
   - Set the path for the encrypted output file (`encryptedData`).
   - Generate a secret key (`scrtkey`) using the DES algorithm with the KeyGenerator class.
   - Define an initialization vector (`initialization_vector`) for added security.

2. **Create Cipher Instance for Encryption:**
   - Initialize the encryption Cipher (`encrypt`) in CBC mode with PKCS5Padding.
   - Set the encryption mode and parameters (secret key and initialization vector) for the Cipher instance.

3. **Perform Encryption:**
   - Open an input stream for the plaintext file (`textFile`).
   - Open an output stream for the encrypted file (`encryptedData`).
   - Create a CipherOutputStream using the encryption Cipher and the output stream.
   - Read the plaintext file in chunks and write the encrypted data to the output file.

4. **Close Streams:**
   - Close the CipherOutputStream, input stream, and output stream.

#### Decryption Algorithm:

1. **Initialize Parameters:**
   - Set the path of the encrypted file (`encryptedData`).
   - Set the path for the decrypted output file (`decryptedData`).

2. **Create Cipher Instance for Decryption:**
   - Initialize the decryption Cipher (`decrypt`) in CBC mode with PKCS5Padding.
   - Set the decryption mode and parameters (secret key and initialization vector) for the Cipher instance.

3. **Perform Decryption:**
   - Open an input stream for the encrypted file (`encryptedData`).
   - Open an output stream for the decrypted file (`decryptedData`).
   - Create a CipherInputStream using the decryption Cipher and the input stream.
   - Read the encrypted file in chunks and write the decrypted data to the output file.

4. **Close Streams:**
   - Close the CipherInputStream, input stream, and output stream.

#### Main Execution:

1. **Main Method:**
   - Set the paths for the plaintext, encrypted, and decrypted files.
   - Generate secret key and initialization vector.
   - Initialize encryption and decryption Ciphers with the generated key and vector.

2. **Encryption:**
   - Call the `encryption` method with the input stream from the plaintext file and the output stream to the encrypted file.

3. **Decryption:**
   - Call the `decryption` method with the input stream from the encrypted file and the output stream to the decrypted file.

4. **Print Success Message:**
   - Print a success message indicating that the encryption and decryption processes have been completed.

5. **Exception Handling:**
   - Catch and handle exceptions related to NoSuchAlgorithmException, NoSuchPaddingException, InvalidKeyException, InvalidAlgorithmParameterException, and IOException.
   - Print any exception messages if encountered.

This algorithm outlines the steps involved in encrypting and decrypting a file using the DES algorithm with Java's Cipher class and related cryptographic APIs.
