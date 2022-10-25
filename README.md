# xml-to-csv
This is a script that parses technical metadata from an xml file to a csv sheet. This format allows us to more easily ingest technical information gathered from our AV vendor as metadata into our digital repostiory.
## What it is
Our vendor creates an xml file in which they record technical information about the av material as they inspect it for digitization. We wanted to be able to more easily ingest this information into our repository as metadata. This includes information such as running speed, stock, condition notes, transfer comments, duration, etc. The vendor usually includes mulitple partners from a particular grant cycle on a hard drive, based on the original shipments we sent to them. These batches are then given a job number and the associated hard drive is named after that job number. The script is run on the hard drive and is able to go through each folder, find the vendor-md.xml file, gather particular information from that file, and put it into a csv file that we can use to copy and paste from into an ingestible spreadsheet for our repository.
## When to use it
This script is a companion to the QC process for digitized files. It was written to talk with hard drives that we get from the vendor. Before we begin QCing the digitized files, we use this script to access the vendor's information. Prior to this script, we were manually opening the PBCore xml files for each object, searching through the file, and copying over some of the information into a spreadsheet. This script reduces repetitive manual work and reduces human error. It's also helpful for reviewing this metadata on a batch level upon receipt of the hard drive.

This script can be used on any hard drive prepared for us by our AV vendor, but it is particularly useful in the 20/21 grant cycle or earlier. Starting in cycle 21/22, the vendor will prepare a csv that we can open and transfer over into one of our ingestible exports. Unlike this script, which is able to gather information from multiple partners and multiple formats into one sheet, our vendor provides up to three csvs, seperated by format type: audio, video, and film.
### Side note
Currently, we still need to do some manual work for multiple item objects. Currently, our system ingests on an object level, not an item level.
#Procedures
1. You will need python3 to be able to run this script.
2. Download the script from this github: xml-to-csv.py
3. Create a folder called "scripts" in your Documents folder. Move xml-to-csv.py to this folder.
4. Plug in the hard drive from the vendor.
5. Open terminal. 
