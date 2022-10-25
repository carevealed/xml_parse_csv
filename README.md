# xml-to-csv
# What it is
This is a script that parses our audiovisual vendor xml to a csv. Our vendor creates an xml file in which they record technical information about the av material as they inspect it for digitization. We wanted to be able to more easily ingest this information into our repository. This includes information such as running speed, stock, condition notes, transfer comments, duration, etc.
#When to use it
This script is a companion to the QC process for digitized files. It was written to talk with HDDs that we get from the vendor. The vendor usually includes mulitple partners from a particular grant cycle. The script is able to go through each folder for each organization and give us one csv that we can use to copy and paste from into an ingestible spreadsheet.

This script can be used on any hard drive prepared for us by our AV vendor, but it is particularly useful in the 20/21 grant cycle or earlier. Starting in cycle 21/22, the vendor will prepare a csv that we can open and transfer over into one of our ingestible exports. Unlike this script, which is able to gather information from multiple partners and multiple formats into one sheet, our vendor provides up to three csvs, seperated by format type: audio, video, and film.
# How to use it
Currently, we still need to do some manual work for multiple item objects. Currently, our system ingests on an object level, not an item level.
