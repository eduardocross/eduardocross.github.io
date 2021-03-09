---
title: DdsSignature Data Storage Considerations

Id: amfUnderSignatureDataStorage
TocParent: amfUnderstandingSignatures
TocOrder: 10

keywords: ASNA Signature Control
keywords: Signatures Storage
keywords: DdsSignatures Storage
keywords: Signatures File Types

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# DdsSignature Data Storage Special Considerations

### Image Format: SVG (Default)
By default, each signature entered into a DdsSignature control is captured in a long character field. The name of the field is specified in the <code> **ValueField** </code> property with the default length of 8,192 characters. The contents of the ValueField use SVG image file format. SVG stands for Scalable Vector Graphics, an open standard specification developed by the World Wide Web Consortium (W3C).

SVG images and their behaviors are defined in XML text files.

The following is an excerpt of a Signature captured as an SVG image:
<pre><span style="background-color:aqua">&lt;?xml version="1.0" encoding="UTF-8" standalone="no"?&gt;</span>

<span style="background-color:aqua">&lt;!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"&gt;</span>

SVG &lt;svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="441" height="147" style="display:block"&gt;

&lt;g fill="none" stroke="#000000" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"&gt;

&lt;path d="M 71.11 6.97 c 0 0.12 -0.74 5.18 0 7.11 c 1.6 4.2 5.65 8.84 7.78 13.33 c 1.12 2.36 1.15 5.46 2.22 7.78 c 1.06 2.29 3.2 4.34 4.45 6.66 c 1.32 2.45 2.53 5.07 3.33 7.78 c 4.03 13.66 6.88 27.24 11.11 41.11 c 2.59 8.47 6.47 16.23 8.89 24.45 c 1.26 4.27 1.96 9.22 2.22 13.33 c 0.09 1.39 -0.31 3.39 -1.11 4.45 c -2.18 2.91 -5.99 6.5 -8.89 8.88 c -0.81 0.66 -2.32 1.12 -3.33 1.12 c -1.31 0 -3.17 -0.48 -4.45 -1.12 c -2.23 -1.12 -4.37 -3.38 -6.66 -4.44 c -2.32 -1.07 -5.46 -1.15 -7.78 -2.22 c -2.3 -1.06 -5.33 -2.53 -6.67 -4.45 c -3.33 -4.76 -7.08 -12.12 -8.89 -17.77 c -0.91 -2.84 -0.71 -7.17 0 -10 c 0.64 -2.54 2.41 -6.11 4.45 -7.78 c 5.33 -4.36 13 -8.29 20 -12.22 c 8.61 -4.83 17.59 -8.88 25.55 -13.34 c 0.87 -0.49 1.43 -1.99 2.23 -2.22 c 1.4 -0.4 3.83 0.31 5.55 0 c 2.17 -0.39 6.56 -1.99 6.67 -2.22 c 0.09 -0.18 -4.02 -0.55 -5.56 0 c -3.16 1.13 -8.09 3.29 -10 5.55 c -1.53 1.81 -2.04 6.07 -2.22 8.89 c -0.17 2.76 0.19 6.29 1.11 8.89 c 1.17 3.32 3.19 7.79 5.56 10 c 2.57 2.4 7.62 4.31 11.11 5.56 c 1.25 0.45 3.05 0.25 4.44 0 c 2.54 -0.46 6.24 -0.83 7.78 -2.23 c 1.89 -1.72 3.62 -5.92 4.44 -8.88 c 0.93 -3.33 1.12 -7.58 1.12 -11.12 c 0 -1.79 -0.48 -4.07 -1.12 -5.55 c -0.35 -0.82 -1.81 -1.41 -2.22 -2.22 c -0.59 -1.19 -0.22 -3.74 -1.11 -4.45 c -2.13 -1.7 -6.83 -3.46 -10 -4.44 c -1.29 -0.4 -3.33 -0.37 -4.44 0 c -0.78 0.26 -1.95 1.39 
-2.23 2.22 c -0.69 2.07 -1.11 5.44 -1.11 7.78 c 0 1.05 0.51 3.33 1.11 3.33 c 1.62 0 6.41 -1.88 8.89 -3.33 c 1.64 -0.96 3.61 -2.77 4.45 -4.45 c 1.87 -3.75 4 -9.03 4.44 -13.33 c 0.6 -5.79 0.16 -13.08 -1.11 -18.89 c -1.21 -5.51 -6.37 -16.25 -6.67 -16.67 c -0.15 -0.21 0.19 6.2 1.12 8.89 c 2.27 6.56 6.53 13.08 8.88 20 c 3.97 11.68 7.24 23.7 10 35.56 c 0.92 3.94 0.98 11.94 1.12 12.22 c 0.09 0.18 0.48 -5.24 1.11 -7.78 c 1.22 -4.87 2.55 -9.8 4.44 -14.44 c 2.18 -5.34 5.52 -13.3 7.78 -15.56 c 0.78 -0.78 4.17 1.19 5.55 2.23 c 1.29 0.97 2.55 2.86 3.34 4.44 c 1.35 2.7 1.96 6.37 3.33 8.89 c 0.68 1.25 2.94 2.07 3.33 3.33 c 1.22 3.9 1.16 10.17 2.23 14.45 c 0.29 1.17 1.68 3.44 2.22 3.33 c 0.75 -0.15 2.57 -2.92 3.33 -4.44 c 0.63 -1.25 0.88 -2.92 1.11 -4.45 c 0.9 -5.97 1.73 -11.78 2.23 -17.78 c 0.25 -2.98 -0.64 -8.63 0 -8.89 c 0.62 -0.25 4.42 4.41 5.55 6.67 c 0.88 1.76 0.46 4.73 1.11 6.67 c 0.38 1.15 1.73 2.18 2.22 3.33 c 0.56 1.32 0.87 2.93 1.12 4.45 c 0.5 2.97 0.9 8.99 1.11 8.88 c 0.24 -0.12 0.5 -6.72 1.11 -10 c 0.49 -2.63 1.15 -5.45 2.22 -7.77 c 1.06 -2.3 3.5 -4.32 4.44 -6.67 c 1.9 -4.74 3.33 -15.56 4.45 -15.56 c 1.14 0 4.05 10.21 5.55 15.56 l 4.45 20"/&gt;
&lt;/g&gt;
&lt;/svg&gt;</pre>

The first two lines specify the XML header required to consider a file "Well Formed". This "Well Formed" header unequivocally defines the type of the XML file. To reduce the size of the DdsSignature data storage, this header is omitted. Should you ever want to produce "Well Formed" XML files out of the DdsSignature capture images, you should copy <span style="background-color:aqua">these two lines verbatim</span> from this sample.

An SVG image file, like the one shown above, is generally stored with the file extension .svg.

SVG image files, being XML, contain many repeated fragments of text, so they are well suited for [ValueFieldLength](http://en.wikipedia.org/wiki/Data_compression#Lossless">lossless data compression</a> algorithms. When an SVG image has been compressed with the industry standard <a href="http://en.wikipedia.org/wiki/Gzip">gzip</a> algorithm, it is referred to as an "SVGZ" image and uses the corresponding .svgz filename extension. Conforming SVG 1.1 viewers will display compressed images. An SVGZ file is typically 20 to 50 percent of the original size. W3C provides SVGZ files to test for conformance.

The DdsSignature **ValueField** contain SVG images, which *are not compressed* . Should you desire to reduce the amount of storage your database will require to store signature records, you would have to implement the compression and de-compression yourself.

### Image Quality
SVG images can be rendered in any size retaining high fidelity, this is one of SVG's biggest advantages compared to raster images such as gif, jpeg, png and bitmap.

The <code> **ValueField** </code> contains the SVG with the size in which the signature was captured. The data size depends on the size of the browser window used when signing. On a Mobile device the size will most likely depend on the physical dimensions of the device. The bigger the size of the surface used to capture the image, the greater the amount of SVG data it produces. The default 8,192 characters was selected to allow signatures based on the typical size of a Smart Phone in Landscape orientation. If your users will be mostly running your App in a Desktop Browser, in particular with the Browser zoomed to the maximum, then the 8,192 characters may not be sufficiently large, and a higher value will need to be specified.

The very first line of the SVG includes the dimensions used to capture the signature. It defines the "natural size" of the image, for example:

<code>SVG &lt;svg xmlns="http://www.w3.org/2000/svg" version="1.1" <span style="background-color:aqua">"width="441" height="147"</span> style="display:block"&gt;</code>

The width and height attributes specify the pixel dimensions of the device surface used to capture the signature.

SVG allows transforming the image with very simple attributes, such that it can be rendered in different sizes, without losing any quality. For example, adding the following attribute to the "g" tag on the second line, will instruct the SVG rendering to produce an image twice as big as the 'natural' size:

<code>&lt;g fill="none" stroke="#000000" stroke-width="3" stroke-linecap="round" stroke-linejoin="round" <span style="background-color:aqua">transform="scale(2)"</span>&gt;</code>

Similarly, using a transformation scaling value of <code>0.5</code> will reduce the image to 50% of its "natural size".

### Unexpected Extremely Elaborate Signatures
Right after capturing a Signature, the SVG is produced in memory and the length of the textual representation is calculated. If the length exceeds the value specified in the <code><a href="amfDssSignatureClassValueFieldLengthProperty.html)</code> property, then a warning message will be presented to the user, indicating that the signature drawn is too elaborate (has too many strokes), and it will need to be reduced. The reduction algorithm attempts to remove line segments evenly out of the strokes that compose the signature, to preserve the overall shape of the signature, but as with most reduction processes, it is not guaranteed to produce the best results. If your users are getting the warning frequently, it is highly recommended to either instruct them to reduce the size of their browser window when signing or increase the value of the <code> **ValueFieldLength** </code> property.

### Image Format: JPEG
DdsSignature can now store signatures as JPEGs on the IFS by leveraging RPG's <code>AFPRSC</code> keyword. For details on the function of this keyword, see the relevant [IBM i documentation](https://www.ibm.com/support/knowledgecenter/en/ssw_ibm_i_73/rzakd/rzakdmstafprsc.html). 

This functionality is supported by six new properties:

- **<code>Directory</code>**  &#8211; IFS Image Directory Name
- **<code>DirectoryField</code>**  &#8211; Field name providing the Directory to the IFS image file.
- **<code>DirectoryFieldLength</code>**  &#8211; Length of DirectoryField
- **<code>Name</code>**  &#8211; IFS Image Filename (JPEG format)
- **<code>NameField</code>**  &#8211; Field name providing the Name of the IFS Image file (JPEG format).
- **<code>NameFieldLength</code>**  &#8211; Length of NameField.

These new properties can be used in the following configurations:

- <code>Directory</code> and <code>Name</code> can set hard coded values for stored .JPEGs.
- <code>DirectoryField</code>/<code>DirectoryFieldLength</code> and <code>NameField</code>/<code>NameFieldLength</code> can set fields for programmatically storing .JPEGs.
- <code>Directory</code> and <code>NameField</code>/<code>NameFieldLength</code> can set a hardcoded directory and a dynamic name.
- <code>DirectoryField</code>/<code>DirectoryFieldLength</code> and <code>Name</code> can set a hard coded Name and a dynamic value.

If values for the <code>ValueField</code> and <code>ValueFieldLength</code> properties are provided these newer properties are overridden.

If values for the <code>DirectoryField</code> and <code>NameField</code> properties are provided, the <code>Directory</code> and <code>Name</code> properties are overridden.

### Aspect Ratio
To prevent an image from being distorted (stretched or skewed), the DdsSignature control uses a property named <code>[AspectRatio](amfDdsSignatureClassAspectRatioProperty.html)</code>, which defines the horizontal to vertical proportions of the surface. The default value is <code>"3:1"</code> specifying that the surface used to capture the image is three times as wide with respect to the height. You can indicate any width to height aspect-ratio, to specify different signature shapes.

Once the aspect-ratio is set, the image will always preserve it. For example, typically you would want to capture Signatures on Mobile devices in Landscape orientation, but present the signature at a later time in a portrait designed record. The default styles for the DdsSignature will adjust the signature width to the containing element (typically a DdsPanel), and the height will be computed using the aspect ratio.

### SVG VIEWERS
At any time, you may need to show the Signature, or print it. There are several products that support SVG format. The most readily available is the browser itself; most modern browsers support SVG files. The files do not need to be "Well formed" (i.e. the XML header is not strictly necessary).

To view a captured signature, copy the contents of the <code> **ValueField** </code> to a new text file, save it with the file extension ".svg" and drag-and-drop the file into your favorite Browser (alternatively use a file URL on the Browser Navigation input box), as shown below:

![](Images/DdsSignatureStore.png)
