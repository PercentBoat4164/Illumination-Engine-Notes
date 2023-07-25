### Assignee - Colin McVety

## Class: FileSystemObject
* Attributes -
	* m_path (string)
		* The path to the object.
	* m_size (int)
		* The size of the contents of the object (for files, this means the size of the file. For directories, this will be the size of all the contents of the directory).
	* m_name (string)
		* Name of the object.
* Methods – 
	 * getParentPath()
		* returns the path of the parent directory.
	* getRootPath()
		* returns the path of the root directory.
 


## Class: File 
### Derives from FileSystemObject
* Attributes: 
	* m_extension
		 * file extension, ex. .pdf, .jpg, .json.
	* (Private) m_importer 
		* Assimp::Importer object. Imports 3d model files.
	* (Private) m_stream
		* Std::fstream object. Handles file IO.
* Methods:
	* open()
		* opens a file for reading and writing
	* close()
		* closes a file
	* append(string t_data)
		* adds data (t_data) to the end of a file
	* insert(string t_data, streamsize t_pos)
		* adds data (t_data) at a specified position (t_pos) in a file
	* overwrite(string t_data, streamsize t_pos)
		* overwrites data t_pos characters from the beginning with new data (t_data)
* Templates:
	* All of these should contain a way to import the data type. Refer to file.hpp.
		* IE_FILE_TYPE_MODEL
		* IE_FILE_TYPE_IMAGE
		* IE_FILE_TYPE_AUDIO
		* IE_FILE_TYPE_JSON


## Class: Directory 
### Derives from FileSystemObject
* Attributes – 
	* m_contents (int)
		* the number of FileSystemObjects in a directory
* Methods - 
	* move(string newPath)
		* change the location of a directory 


