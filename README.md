HuffmanEncoder: The code provides the core components for Huffman encoding, allowing data compression with the ability to obtain the encoded data and Huffman tree.
Here's a concise summary of its key components and functionality:
1. **Frequency Table Creation:**
   - The code creates a frequency table to count the occurrences of each character in the input data.
2. **Huffman Tree Building:**
   - It constructs a Huffman tree using a priority queue.
   - Nodes for characters with their frequencies are created and combined until a single root node remains.
3. **Lookup Table Creation:**
   - A lookup table is generated to map characters to their Huffman codes.
   - It traverses the Huffman tree to assign binary codes to each character.
4. **Compression:**
   - The `compress` method compresses input data using Huffman coding.
   - It returns an object containing the encoded data and the Huffman tree's root.
5. **Decompression (Stubbed):**
   - A decompression method is included but currently returns `null` and needs implementation.
6. **Node Class:**
   - Nodes in the Huffman tree are represented with character, frequency, and child nodes.
   - The class provides a method to check if a node is a leaf node.
7. **HuffmanEncodedResult Class:**
   - This class holds the result of Huffman encoding, including the encoded data and Huffman tree's root.
8. **Main Method (Testing):**
   - The `main` method demonstrates the code's functionality by building a Huffman tree and printing its root for a test string.
  
ImageEncoderHuffman: The code demonstrates the application of Huffman encoding to compress image data. It includes both encoding and decoding processes, allowing for the measurement of compression efficiency.
1. **Huffman Encoding:**
   - Reads an image file and encodes its binary data using Huffman encoding.
   - Calculates and displays the compression ratio (percentage).
2. **File Input:**
   - Reads the image file using `FileInputStream` and stores its binary data in a byte array.
3. **Encoding Image Data:**
   - Converts the image's binary data into a URL-safe Base64 encoded string using the `encodeImage` method.
4. **Compression:**
   - Compresses the Base64 encoded image data using Huffman encoding.
   - Returns a `HuffmanEncodedResult` object containing the encoded data and Huffman tree's root.
5. **Decompression:**
   - Decodes the compressed data to retrieve the original image data.
   - Utilizes the Huffman tree stored in the `HuffmanEncodedResult` object to decode the data.
6. **Node Class:**
   - Represents nodes in the Huffman tree, facilitating tree construction and data decoding.
7. **HuffmanEncodedResult Class:**
   - Stores the encoded data and Huffman tree's root.
   - Provides methods to access these properties.
8. **Main Method (Testing):**
   - Reads an image file, encodes it, and decodes it to calculate the compression ratio.
   - Prints the lengths of the encoded and decoded data and the compression percentage.

References: https://commons.apache.org/proper/commons-codec/download_codec.cgi //(to download apache package to covert image to string Base64) https://myjeeva.com/convert-image-to-string-and-string-to-image-in-java.html //(Convert Image to String and String to Image in Java)

The program can compress any file using Huffman Coding algorithm into a stream of 1s and 0s which can then be transferred by simply copying in notepad and then decompressed using the decoder to a Base64 string and then to the original file using Apache commons library# FileCompressor.
