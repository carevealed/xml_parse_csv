# What
This is a script that parses technical metadata from an xml file to a csv sheet. This format allows us to more easily ingest technical information gathered from our AV vendor as metadata into our digital repostiory. This script and directions are written for terminal on MacOS.
# Why
Our vendor creates an xml file in which they record technical information about the av material as they inspect it for digitization. We wanted to be able to more easily ingest this information into our repository as metadata. This includes information such as running speed, stock, condition notes, transfer comments, duration, etc. The vendor usually includes mulitple partners from a particular grant cycle on a hard drive, based on the original shipments we sent to them. These batches are then given a job number and the associated hard drive is named after that job number. The script is run on the hard drive and is able to go through each folder, find the vendor-md.xml file, gather particular information from that file, and put it into a csv file that we can use to copy and paste from into an ingestible spreadsheet for our repository.
# When
This script is a companion to the QC process for digitized files. It was written to talk with hard drives that we get from the vendor. Before we begin QCing the digitized files, we use this script to access the vendor's information. Prior to this script, we were manually opening the PBCore xml files for each object, searching through the file, and copying over some of the information into a spreadsheet. This script reduces repetitive manual work and reduces human error. It's also helpful for reviewing this metadata on a batch level upon receipt of the hard drive.
# Where
This script can be used on any hard drive prepared for us by our AV vendor, but it is particularly useful in the 20/21 grant cycle or earlier. Starting in cycle 21/22, the vendor will prepare a csv that we can open and transfer over into one of our ingestible exports. Unlike this script, which is able to gather information from multiple partners and multiple formats into one sheet, our vendor provides up to three csvs, seperated by format type: audio, video, and film.
## Side note
Currently, the current California Revealed repository can only ingest object level rather than item level metadata. This means we will need to do some manual work for multiple item objects before copying over the information for ingest by combining multiple item objects into one row using our formatting and delimiter rules.
# How
- You will need python3 to be able to run this script
- Download the script from this github: xml_parse_csv.py
- Create a folder called "scripts" in your Documents folder. Move xml_parse_csv.py to this folder.
- Plug in the hard drive from the vendor.
- Open terminal and change your directory (cd) to the scripts folder. You can use the code below to do so.
```
cd Documents/scripts/
```
- Now you are ready to use the script to create the csv. Here is the beginning of the code, which will then be followed by the pathway to the hard drive:
```
python3 xml_parse_csv.py /Volumes/
```
- Right now, the pathway only leads to "Volumes". You will need to type the rest in. Note: pathways are case-sensitive. Type out the name of the hard drive as it shows in Finder and make sure that you add a forward slash at the end of the hard drive name.
Example:
```
python3 xml_parse_csv.py /Volumes/CAR3924/
```
- When you press enter, the terminal will print when the csv and headers are written, how many vendor-md.xml files it found, the pathways to each file, and if any errors came up along the way.
