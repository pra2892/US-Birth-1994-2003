# US-Birth-1994-2003
Guided Project: Explore U.S. Births @python3 @jupyter


# Function Name: read_csv(filname)
# This function will read the content of input csv file,
# clean the data, split the data rows and store into final_list[]

def read_csv(file_name):
    data = open(file_name).read()
    string_list = data.split("\n")
    string_list = string_list[1:len(string_list)]
    final_list = []
    
    for line in string_list:
        int_fields = []
        string_fields = line.split(",")
        
        for line1 in string_fields:
            int_fields.append(int(line1))
            
        final_list.append(int_fields)
    
    return(final_list)

cdc_list = read_csv("US_births_1994-2003_CDC_NCHS.csv")
cdc_list
Out[24]:
[[1994, 1, 1, 6, 8096],
 [1994, 1, 2, 7, 7772],
 [1994, 1, 3, 1, 10142],
 [1994, 1, 4, 2, 11248],
 [1994, 1, 5, 3, 11053],
 [1994, 1, 6, 4, 11406],
 [1994, 1, 7, 5, 11251],
 [1994, 1, 8, 6, 8653],
 [1994, 1, 9, 7, 7910],
 [1994, 1, 10, 1, 10498],
 [1994, 1, 11, 2, 11706],
 [1994, 1, 12, 3, 11567],
 [1994, 1, 13, 4, 11212],
 [1994, 1, 14, 5, 11570],
 [1994, 1, 15, 6, 8660],
 [1994, 1, 16, 7, 8123],
 [1994, 1, 17, 1, 10567],
 [1994, 1, 18, 2, 11541],
 [1994, 1, 19, 3, 11257],
 [1994, 1, 20, 4, 11682],
 [1994, 1, 21, 5, 11811],
 [1994, 1, 22, 6, 8833],
 [1994, 1, 23, 7, 8310],
 [1994, 1, 24, 1, 11125],
 [1994, 1, 25, 2, 11981],
 [1994, 1, 26, 3, 11514],
 [1994, 1, 27, 4, 11702],
 [1994, 1, 28, 5, 11666],
 [1994, 1, 29, 6, 8988],
 [1994, 1, 30, 7, 8096],
 [1994, 1, 31, 1, 10765],
 [1994, 2, 1, 2, 11755],
 [1994, 2, 2, 3, 11483],
 [1994, 2, 3, 4, 11523],
 [1994, 2, 4, 5, 11677],
 [1994, 2, 5, 6, 8991],
 [1994, 2, 6, 7, 8309],
 [1994, 2, 7, 1, 10984],
 [1994, 2, 8, 2, 12152],
 [1994, 2, 9, 3, 11515],
 [1994, 2, 10, 4, 11623],
 [1994, 2, 11, 5, 11517],
 [1994, 2, 12, 6, 8945],
 [1994, 2, 13, 7, 8171],
 [1994, 2, 14, 1, 11551],
 [1994, 2, 15, 2, 12164],
 [1994, 2, 16, 3, 12009],
 [1994, 2, 17, 4, 11674],
 [1994, 2, 18, 5, 11887],
 [1994, 2, 19, 6, 8946],
 [1994, 2, 20, 7, 8402],
 [1994, 2, 21, 1, 10617],
 [1994, 2, 22, 2, 11810],
 [1994, 2, 23, 3, 11776],
 [1994, 2, 24, 4, 11667],
 [1994, 2, 25, 5, 11905],
 [1994, 2, 26, 6, 8988],
 [1994, 2, 27, 7, 8195],
 [1994, 2, 28, 1, 11091],
 [1994, 3, 1, 2, 12127],
 [1994, 3, 2, 3, 11735],
 [1994, 3, 3, 4, 11984],
 [1994, 3, 4, 5, 12066],
 [1994, 3, 5, 6, 9215],
 [1994, 3, 6, 7, 8389],
 [1994, 3, 7, 1, 10996],
 [1994, 3, 8, 2, 12275],
 [1994, 3, 9, 3, 11780],
 [1994, 3, 10, 4, 11792],
 [1994, 3, 11, 5, 11939],
 [1994, 3, 12, 6, 9087],
 [1994, 3, 13, 7, 8248],
 [1994, 3, 14, 1, 11092],
 [1994, 3, 15, 2, 12298],
 [1994, 3, 16, 3, 11865],
 [1994, 3, 17, 4, 11976],
 [1994, 3, 18, 5, 11799],
 [1994, 3, 19, 6, 8944],
 [1994, 3, 20, 7, 8243],
 [1994, 3, 21, 1, 11140],
 [1994, 3, 22, 2, 11964],
 [1994, 3, 23, 3, 11637],
 [1994, 3, 24, 4, 11904],
 [1994, 3, 25, 5, 11568],
 [1994, 3, 26, 6, 8957],
 [1994, 3, 27, 7, 8189],
 [1994, 3, 28, 1, 11051],
 [1994, 3, 29, 2, 12154],
 [1994, 3, 30, 3, 11540],
 [1994, 3, 31, 4, 11782],
 [1994, 4, 1, 5, 10630],
 [1994, 4, 2, 6, 8782],
 [1994, 4, 3, 7, 7530],
 [1994, 4, 4, 1, 10909],
 [1994, 4, 5, 2, 11876],
 [1994, 4, 6, 3, 11811],
 [1994, 4, 7, 4, 11718],
 [1994, 4, 8, 5, 11532],
 [1994, 4, 9, 6, 8791],
 [1994, 4, 10, 7, 8183],
 [1994, 4, 11, 1, 11060],
 [1994, 4, 12, 2, 12146],
 [1994, 4, 13, 3, 11428],
 [1994, 4, 14, 4, 11709],
 [1994, 4, 15, 5, 11753],
 [1994, 4, 16, 6, 8790],
 [1994, 4, 17, 7, 7867],
 [1994, 4, 18, 1, 11094],
 [1994, 4, 19, 2, 11966],
 [1994, 4, 20, 3, 11585],
 [1994, 4, 21, 4, 11509],
 [1994, 4, 22, 5, 11553],
 [1994, 4, 23, 6, 8613],
 [1994, 4, 24, 7, 8089],
 [1994, 4, 25, 1, 10909],
 [1994, 4, 26, 2, 12236],
 [1994, 4, 27, 3, 11701],
 [1994, 4, 28, 4, 11527],
 [1994, 4, 29, 5, 11474],
 [1994, 4, 30, 6, 8621],
 [1994, 5, 1, 7, 8145],
 [1994, 5, 2, 1, 11169],
 [1994, 5, 3, 2, 12023],
 [1994, 5, 4, 3, 11754],
 [1994, 5, 5, 4, 11958],
 [1994, 5, 6, 5, 11904],
 [1994, 5, 7, 6, 8641],
 [1994, 5, 8, 7, 8203],
 [1994, 5, 9, 1, 10914],
 [1994, 5, 10, 2, 11771],
 [1994, 5, 11, 3, 11278],
 [1994, 5, 12, 4, 11822],
 [1994, 5, 13, 5, 11085],
 [1994, 5, 14, 6, 8830],
 [1994, 5, 15, 7, 8253],
 [1994, 5, 16, 1, 11103],
 [1994, 5, 17, 2, 12289],
 [1994, 5, 18, 3, 11668],
 [1994, 5, 19, 4, 11411],
 [1994, 5, 20, 5, 11645],
 [1994, 5, 21, 6, 8830],
 [1994, 5, 22, 7, 8449],
 [1994, 5, 23, 1, 11434],
 [1994, 5, 24, 2, 12562],
 [1994, 5, 25, 3, 12005],
 [1994, 5, 26, 4, 11979],
 [1994, 5, 27, 5, 12132],
 [1994, 5, 28, 6, 8840],
 [1994, 5, 29, 7, 8205],
 [1994, 5, 30, 1, 8468],
 [1994, 5, 31, 2, 11525],
 [1994, 6, 1, 3, 12349],
 [1994, 6, 2, 4, 12166],
 [1994, 6, 3, 5, 11799],
 [1994, 6, 4, 6, 9182],
 [1994, 6, 5, 7, 8289],
 [1994, 6, 6, 1, 11130],
 [1994, 6, 7, 2, 12145],
 [1994, 6, 8, 3, 11784],
 [1994, 6, 9, 4, 11648],
 [1994, 6, 10, 5, 12006],
 [1994, 6, 11, 6, 8618],
 [1994, 6, 12, 7, 8171],
 [1994, 6, 13, 1, 10692],
 [1994, 6, 14, 2, 12074],
 [1994, 6, 15, 3, 11954],
 [1994, 6, 16, 4, 11852],
 [1994, 6, 17, 5, 11744],
 [1994, 6, 18, 6, 8907],
 [1994, 6, 19, 7, 8302],
 [1994, 6, 20, 1, 11337],
 [1994, 6, 21, 2, 12182],
 [1994, 6, 22, 3, 12213],
 [1994, 6, 23, 4, 11939],
 [1994, 6, 24, 5, 11979],
 [1994, 6, 25, 6, 9047],
 [1994, 6, 26, 7, 8306],
 [1994, 6, 27, 1, 11309],
 [1994, 6, 28, 2, 12211],
 [1994, 6, 29, 3, 12245],
 [1994, 6, 30, 4, 12157],
 [1994, 7, 1, 5, 12454],
 [1994, 7, 2, 6, 9268],
 [1994, 7, 3, 7, 8298],
 [1994, 7, 4, 1, 8564],
 [1994, 7, 5, 2, 11609],
 [1994, 7, 6, 3, 13086],
 [1994, 7, 7, 4, 13049],
 [1994, 7, 8, 5, 12623],
 [1994, 7, 9, 6, 9325],
 [1994, 7, 10, 7, 8684],
 [1994, 7, 11, 1, 11567],
 [1994, 7, 12, 2, 12507],
 [1994, 7, 13, 3, 12134],
 [1994, 7, 14, 4, 12485],
 [1994, 7, 15, 5, 12691],
 [1994, 7, 16, 6, 9547],
 [1994, 7, 17, 7, 8848],
 [1994, 7, 18, 1, 11561],
 [1994, 7, 19, 2, 12583],
 [1994, 7, 20, 3, 12378],
 [1994, 7, 21, 4, 12447],
 [1994, 7, 22, 5, 12486],
 [1994, 7, 23, 6, 9463],
 [1994, 7, 24, 7, 8734],
 [1994, 7, 25, 1, 11757],
 [1994, 7, 26, 2, 12591],
 [1994, 7, 27, 3, 12423],
 [1994, 7, 28, 4, 12539],
 [1994, 7, 29, 5, 12231],
 [1994, 7, 30, 6, 9340],
 [1994, 7, 31, 7, 8590],
 [1994, 8, 1, 1, 11428],
 [1994, 8, 2, 2, 12622],
 [1994, 8, 3, 3, 12147],
 [1994, 8, 4, 4, 12601],
 [1994, 8, 5, 5, 12251],
 [1994, 8, 6, 6, 9336],
 [1994, 8, 7, 7, 8517],
 [1994, 8, 8, 1, 11528],
 [1994, 8, 9, 2, 12643],
 [1994, 8, 10, 3, 12525],
 [1994, 8, 11, 4, 12147],
 [1994, 8, 12, 5, 12479],
 [1994, 8, 13, 6, 9474],
 [1994, 8, 14, 7, 8926],
 [1994, 8, 15, 1, 11391],
 [1994, 8, 16, 2, 12605],
 [1994, 8, 17, 3, 12344],
 [1994, 8, 18, 4, 12313],
 [1994, 8, 19, 5, 12227],
 [1994, 8, 20, 6, 9646],
 [1994, 8, 21, 7, 8663],
 [1994, 8, 22, 1, 11489],
 [1994, 8, 23, 2, 12284],
 [1994, 8, 24, 3, 12176],
 [1994, 8, 25, 4, 12076],
 [1994, 8, 26, 5, 12122],
 [1994, 8, 27, 6, 9171],
 [1994, 8, 28, 7, 8779],
 [1994, 8, 29, 1, 11560],
 [1994, 8, 30, 2, 12431],
 [1994, 8, 31, 3, 12272],
 [1994, 9, 1, 4, 12183],
 [1994, 9, 2, 5, 12099],
 [1994, 9, 3, 6, 9042],
 [1994, 9, 4, 7, 8420],
 [1994, 9, 5, 1, 8378],
 [1994, 9, 6, 2, 11448],
 [1994, 9, 7, 3, 12660],
 [1994, 9, 8, 4, 12693],
 [1994, 9, 9, 5, 12811],
 [1994, 9, 10, 6, 9424],
 [1994, 9, 11, 7, 8373],
 [1994, 9, 12, 1, 11500],
 [1994, 9, 13, 2, 12560],
 [1994, 9, 14, 3, 12566],
 [1994, 9, 15, 4, 12655],
 [1994, 9, 16, 5, 12884],
 [1994, 9, 17, 6, 9779],
 [1994, 9, 18, 7, 8603],
 [1994, 9, 19, 1, 11659],
 [1994, 9, 20, 2, 12584],
 [1994, 9, 21, 3, 12468],
 [1994, 9, 22, 4, 12590],
 [1994, 9, 23, 5, 12522],
 [1994, 9, 24, 6, 9597],
 [1994, 9, 25, 7, 8754],
 [1994, 9, 26, 1, 11597],
 [1994, 9, 27, 2, 12591],
 [1994, 9, 28, 3, 12405],
 [1994, 9, 29, 4, 12288],
 [1994, 9, 30, 5, 12090],
 [1994, 10, 1, 6, 9351],
 [1994, 10, 2, 7, 8477],
 [1994, 10, 3, 1, 11437],
 [1994, 10, 4, 2, 12378],
 [1994, 10, 5, 3, 12061],
 [1994, 10, 6, 4, 12017],
 [1994, 10, 7, 5, 12050],
 [1994, 10, 8, 6, 8981],
 [1994, 10, 9, 7, 8038],
 [1994, 10, 10, 1, 11110],
 [1994, 10, 11, 2, 12236],
 [1994, 10, 12, 3, 11846],
 [1994, 10, 13, 4, 11398],
 [1994, 10, 14, 5, 11959],
 [1994, 10, 15, 6, 9077],
 [1994, 10, 16, 7, 8022],
 [1994, 10, 17, 1, 11127],
 [1994, 10, 18, 2, 11888],
 [1994, 10, 19, 3, 11533],
 [1994, 10, 20, 4, 11876],
 [1994, 10, 21, 5, 11562],
 [1994, 10, 22, 6, 9086],
 [1994, 10, 23, 7, 7914],
 [1994, 10, 24, 1, 11068],
 [1994, 10, 25, 2, 12019],
 [1994, 10, 26, 3, 11683],
 [1994, 10, 27, 4, 11420],
 [1994, 10, 28, 5, 11608],
 [1994, 10, 29, 6, 8855],
 [1994, 10, 30, 7, 8262],
 [1994, 10, 31, 1, 9833],
 [1994, 11, 1, 2, 12316],
 [1994, 11, 2, 3, 11736],
 [1994, 11, 3, 4, 11703],
 [1994, 11, 4, 5, 11956],
 [1994, 11, 5, 6, 8826],
 [1994, 11, 6, 7, 8100],
 [1994, 11, 7, 1, 11283],
 [1994, 11, 8, 2, 11999],
 [1994, 11, 9, 3, 11811],
 [1994, 11, 10, 4, 11728],
 [1994, 11, 11, 5, 11533],
 [1994, 11, 12, 6, 8672],
 [1994, 11, 13, 7, 8093],
 [1994, 11, 14, 1, 11044],
 [1994, 11, 15, 2, 11985],
 [1994, 11, 16, 3, 11634],
 [1994, 11, 17, 4, 11703],
 [1994, 11, 18, 5, 11826],
 [1994, 11, 19, 6, 8771],
 [1994, 11, 20, 7, 8133],
 [1994, 11, 21, 1, 11807],
 [1994, 11, 22, 2, 12764],
 [1994, 11, 23, 3, 11332],
 [1994, 11, 24, 4, 8036],
 [1994, 11, 25, 5, 9419],
 [1994, 11, 26, 6, 8427],
 [1994, 11, 27, 7, 7937],
 [1994, 11, 28, 1, 11003],
 [1994, 11, 29, 2, 12177],
 [1994, 11, 30, 3, 11643],
 [1994, 12, 1, 4, 11681],
 [1994, 12, 2, 5, 11379],
 [1994, 12, 3, 6, 8585],
 [1994, 12, 4, 7, 7980],
 [1994, 12, 5, 1, 10772],
 [1994, 12, 6, 2, 11923],
 [1994, 12, 7, 3, 11335],
 [1994, 12, 8, 4, 11337],
 [1994, 12, 9, 5, 11205],
 [1994, 12, 10, 6, 8461],
 [1994, 12, 11, 7, 7936],
 [1994, 12, 12, 1, 11106],
 [1994, 12, 13, 2, 11884],
 [1994, 12, 14, 3, 11716],
 [1994, 12, 15, 4, 11962],
 [1994, 12, 16, 5, 12144],
 [1994, 12, 17, 6, 8726],
 [1994, 12, 18, 7, 8130],
 [1994, 12, 19, 1, 11502],
 [1994, 12, 20, 2, 12880],
 [1994, 12, 21, 3, 12391],
 [1994, 12, 22, 4, 11504],
 [1994, 12, 23, 5, 10087],
 [1994, 12, 24, 6, 7898],
 [1994, 12, 25, 7, 7192],
 [1994, 12, 26, 1, 8454],
 [1994, 12, 27, 2, 11131],
 [1994, 12, 28, 3, 12398],
 [1994, 12, 29, 4, 12189],
 [1994, 12, 30, 5, 12051],
 [1994, 12, 31, 6, 8809],
 [1995, 1, 1, 7, 7828],
 [1995, 1, 2, 1, 7883],
 [1995, 1, 3, 2, 9999],
 [1995, 1, 4, 3, 11315],
 [1995, 1, 5, 4, 11243],
 [1995, 1, 6, 5, 11506],
 [1995, 1, 7, 6, 8681],
 [1995, 1, 8, 7, 7821],
 [1995, 1, 9, 1, 10434],
 [1995, 1, 10, 2, 11665],
 [1995, 1, 11, 3, 11279],
 [1995, 1, 12, 4, 11416],
 [1995, 1, 13, 5, 11071],
 [1995, 1, 14, 6, 8887],
 [1995, 1, 15, 7, 7988],
 [1995, 1, 16, 1, 10417],
 [1995, 1, 17, 2, 11345],
 [1995, 1, 18, 3, 11252],
 [1995, 1, 19, 4, 11331],
 [1995, 1, 20, 5, 11481],
 [1995, 1, 21, 6, 8746],
 [1995, 1, 22, 7, 7956],
 [1995, 1, 23, 1, 10640],
 [1995, 1, 24, 2, 11344],
 [1995, 1, 25, 3, 11096],
 [1995, 1, 26, 4, 11380],
 [1995, 1, 27, 5, 11340],
 [1995, 1, 28, 6, 8781],
 [1995, 1, 29, 7, 8009],
 [1995, 1, 30, 1, 10515],
 [1995, 1, 31, 2, 11364],
 [1995, 2, 1, 3, 11279],
 [1995, 2, 2, 4, 11490],
 [1995, 2, 3, 5, 11264],
 [1995, 2, 4, 6, 8769],
 [1995, 2, 5, 7, 8017],
 [1995, 2, 6, 1, 10587],
 [1995, 2, 7, 2, 11483],
 [1995, 2, 8, 3, 11205],
 [1995, 2, 9, 4, 11282],
 [1995, 2, 10, 5, 11615],
 [1995, 2, 11, 6, 8949],
 [1995, 2, 12, 7, 8007],
 [1995, 2, 13, 1, 10351],
 [1995, 2, 14, 2, 12454],
 [1995, 2, 15, 3, 11828],
 [1995, 2, 16, 4, 11657],
 [1995, 2, 17, 5, 11625],
 [1995, 2, 18, 6, 8788],
 [1995, 2, 19, 7, 8038],
 [1995, 2, 20, 1, 10258],
 [1995, 2, 21, 2, 11582],
 [1995, 2, 22, 3, 11716],
 [1995, 2, 23, 4, 11786],
 [1995, 2, 24, 5, 11671],
 [1995, 2, 25, 6, 8829],
 [1995, 2, 26, 7, 8183],
 [1995, 2, 27, 1, 10702],
 [1995, 2, 28, 2, 11679],
 [1995, 3, 1, 3, 11540],
 [1995, 3, 2, 4, 11377],
 [1995, 3, 3, 5, 11649],
 [1995, 3, 4, 6, 8807],
 [1995, 3, 5, 7, 7984],
 [1995, 3, 6, 1, 10810],
 [1995, 3, 7, 2, 12115],
 [1995, 3, 8, 3, 11618],
 [1995, 3, 9, 4, 11380],
 [1995, 3, 10, 5, 11827],
 [1995, 3, 11, 6, 8744],
 [1995, 3, 12, 7, 7859],
 [1995, 3, 13, 1, 10609],
 [1995, 3, 14, 2, 11750],
 [1995, 3, 15, 3, 11736],
 [1995, 3, 16, 4, 11751],
 [1995, 3, 17, 5, 11953],
 [1995, 3, 18, 6, 8538],
 [1995, 3, 19, 7, 7787],
 [1995, 3, 20, 1, 10588],
 [1995, 3, 21, 2, 11837],
 [1995, 3, 22, 3, 11485],
 [1995, 3, 23, 4, 11435],
 [1995, 3, 24, 5, 11329],
 [1995, 3, 25, 6, 8628],
 [1995, 3, 26, 7, 7614],
 [1995, 3, 27, 1, 10541],
 [1995, 3, 28, 2, 11563],
 [1995, 3, 29, 3, 11125],
 [1995, 3, 30, 4, 11205],
 [1995, 3, 31, 5, 11319],
 [1995, 4, 1, 6, 8398],
 [1995, 4, 2, 7, 7547],
 [1995, 4, 3, 1, 10651],
 [1995, 4, 4, 2, 11960],
 [1995, 4, 5, 3, 11475],
 [1995, 4, 6, 4, 11429],
 [1995, 4, 7, 5, 11587],
 [1995, 4, 8, 6, 8588],
 [1995, 4, 9, 7, 7839],
 [1995, 4, 10, 1, 10930],
 [1995, 4, 11, 2, 11939],
 [1995, 4, 12, 3, 11750],
 [1995, 4, 13, 4, 11411],
 [1995, 4, 14, 5, 10687],
 [1995, 4, 15, 6, 8492],
 [1995, 4, 16, 7, 7503],
 [1995, 4, 17, 1, 10640],
 [1995, 4, 18, 2, 11652],
 [1995, 4, 19, 3, 11680],
 [1995, 4, 20, 4, 11504],
 [1995, 4, 21, 5, 11445],
 [1995, 4, 22, 6, 8560],
 [1995, 4, 23, 7, 7749],
 [1995, 4, 24, 1, 11014],
 [1995, 4, 25, 2, 11811],
 [1995, 4, 26, 3, 11551],
 [1995, 4, 27, 4, 11601],
 [1995, 4, 28, 5, 11457],
 [1995, 4, 29, 6, 8492],
 [1995, 4, 30, 7, 7777],
 [1995, 5, 1, 1, 11090],
 [1995, 5, 2, 2, 12119],
 [1995, 5, 3, 3, 11502],
 [1995, 5, 4, 4, 11800],
 [1995, 5, 5, 5, 11718],
 [1995, 5, 6, 6, 8565],
 [1995, 5, 7, 7, 7965],
 [1995, 5, 8, 1, 10790],
 [1995, 5, 9, 2, 11728],
 [1995, 5, 10, 3, 11723],
 [1995, 5, 11, 4, 11723],
 [1995, 5, 12, 5, 11625],
 [1995, 5, 13, 6, 8802],
 [1995, 5, 14, 7, 8165],
 [1995, 5, 15, 1, 11143],
 [1995, 5, 16, 2, 12101],
 [1995, 5, 17, 3, 12085],
 [1995, 5, 18, 4, 11872],
 [1995, 5, 19, 5, 11692],
 [1995, 5, 20, 6, 8721],
 [1995, 5, 21, 7, 8096],
 [1995, 5, 22, 1, 11250],
 [1995, 5, 23, 2, 12539],
 [1995, 5, 24, 3, 12193],
 [1995, 5, 25, 4, 12285],
 [1995, 5, 26, 5, 12246],
 [1995, 5, 27, 6, 8795],
 [1995, 5, 28, 7, 8167],
 [1995, 5, 29, 1, 8379],
 [1995, 5, 30, 2, 11271],
 [1995, 5, 31, 3, 12393],
 [1995, 6, 1, 4, 12243],
 [1995, 6, 2, 5, 11991],
 [1995, 6, 3, 6, 9069],
 [1995, 6, 4, 7, 8059],
 [1995, 6, 5, 1, 11152],
 [1995, 6, 6, 2, 12119],
 [1995, 6, 7, 3, 11774],
 [1995, 6, 8, 4, 12031],
 [1995, 6, 9, 5, 11645],
 [1995, 6, 10, 6, 8719],
 [1995, 6, 11, 7, 8149],
 [1995, 6, 12, 1, 11169],
 [1995, 6, 13, 2, 11790],
 [1995, 6, 14, 3, 11958],
 [1995, 6, 15, 4, 11906],
 [1995, 6, 16, 5, 11856],
 [1995, 6, 17, 6, 8821],
 [1995, 6, 18, 7, 8203],
 [1995, 6, 19, 1, 11223],
 [1995, 6, 20, 2, 12395],
 [1995, 6, 21, 3, 12049],
 [1995, 6, 22, 4, 11799],
 [1995, 6, 23, 5, 11942],
 [1995, 6, 24, 6, 9065],
 [1995, 6, 25, 7, 8279],
 [1995, 6, 26, 1, 11127],
 [1995, 6, 27, 2, 12349],
 [1995, 6, 28, 3, 12162],
 [1995, 6, 29, 4, 12423],
 [1995, 6, 30, 5, 12338],
 [1995, 7, 1, 6, 9283],
 [1995, 7, 2, 7, 8256],
 [1995, 7, 3, 1, 10623],
 [1995, 7, 4, 2, 9374],
 [1995, 7, 5, 3, 11399],
 [1995, 7, 6, 4, 12855],
 [1995, 7, 7, 5, 12954],
 [1995, 7, 8, 6, 9438],
 [1995, 7, 9, 7, 8506],
 [1995, 7, 10, 1, 11618],
 [1995, 7, 11, 2, 12552],
 [1995, 7, 12, 3, 12167],
 [1995, 7, 13, 4, 12253],
 [1995, 7, 14, 5, 12659],
 [1995, 7, 15, 6, 9391],
 [1995, 7, 16, 7, 8516],
 [1995, 7, 17, 1, 11461],
 [1995, 7, 18, 2, 12495],
 [1995, 7, 19, 3, 12129],
 [1995, 7, 20, 4, 12598],
 [1995, 7, 21, 5, 12428],
 [1995, 7, 22, 6, 9328],
 [1995, 7, 23, 7, 8483],
 [1995, 7, 24, 1, 11501],
 [1995, 7, 25, 2, 12580],
 [1995, 7, 26, 3, 12316],
 [1995, 7, 27, 4, 12309],
 [1995, 7, 28, 5, 12442],
 [1995, 7, 29, 6, 9277],
 [1995, 7, 30, 7, 8384],
 [1995, 7, 31, 1, 11298],
 [1995, 8, 1, 2, 12442],
 [1995, 8, 2, 3, 12249],
 [1995, 8, 3, 4, 12193],
 [1995, 8, 4, 5, 12186],
 [1995, 8, 5, 6, 9267],
 [1995, 8, 6, 7, 8346],
 [1995, 8, 7, 1, 11223],
 [1995, 8, 8, 2, 12441],
 [1995, 8, 9, 3, 12217],
 [1995, 8, 10, 4, 12243],
 [1995, 8, 11, 5, 12154],
 [1995, 8, 12, 6, 9153],
 [1995, 8, 13, 7, 8421],
 [1995, 8, 14, 1, 11297],
 [1995, 8, 15, 2, 12760],
 [1995, 8, 16, 3, 12244],
 [1995, 8, 17, 4, 12345],
 [1995, 8, 18, 5, 12362],
 [1995, 8, 19, 6, 9265],
 [1995, 8, 20, 7, 8434],
 [1995, 8, 21, 1, 11436],
 [1995, 8, 22, 2, 12612],
 [1995, 8, 23, 3, 12083],
 [1995, 8, 24, 4, 12381],
 [1995, 8, 25, 5, 12208],
 [1995, 8, 26, 6, 9155],
 [1995, 8, 27, 7, 8509],
 [1995, 8, 28, 1, 11473],
 [1995, 8, 29, 2, 12522],
 [1995, 8, 30, 3, 12631],
 [1995, 8, 31, 4, 12485],
 [1995, 9, 1, 5, 12439],
 [1995, 9, 2, 6, 9079],
 [1995, 9, 3, 7, 8438],
 [1995, 9, 4, 1, 8441],
 [1995, 9, 5, 2, 11682],
 [1995, 9, 6, 3, 12951],
 [1995, 9, 7, 4, 12924],
 [1995, 9, 8, 5, 12939],
 [1995, 9, 9, 6, 9714],
 [1995, 9, 10, 7, 8568],
 [1995, 9, 11, 1, 11480],
 [1995, 9, 12, 2, 12583],
 [1995, 9, 13, 3, 12173],
 [1995, 9, 14, 4, 12789],
 [1995, 9, 15, 5, 13023],
 [1995, 9, 16, 6, 9535],
 [1995, 9, 17, 7, 8757],
 [1995, 9, 18, 1, 11729],
 [1995, 9, 19, 2, 12692],
 [1995, 9, 20, 3, 12571],
 [1995, 9, 21, 4, 12663],
 [1995, 9, 22, 5, 12813],
 [1995, 9, 23, 6, 9341],
 [1995, 9, 24, 7, 8659],
 [1995, 9, 25, 1, 11552],
 [1995, 9, 26, 2, 12814],
 [1995, 9, 27, 3, 12605],
 [1995, 9, 28, 4, 12845],
 [1995, 9, 29, 5, 12316],
 [1995, 9, 30, 6, 8988],
 [1995, 10, 1, 7, 8545],
 [1995, 10, 2, 1, 11650],
 [1995, 10, 3, 2, 12375],
 [1995, 10, 4, 3, 12016],
 [1995, 10, 5, 4, 12245],
 [1995, 10, 6, 5, 12081],
 [1995, 10, 7, 6, 9048],
 [1995, 10, 8, 7, 7997],
 [1995, 10, 9, 1, 10892],
 [1995, 10, 10, 2, 12273],
 [1995, 10, 11, 3, 11843],
 [1995, 10, 12, 4, 12002],
 [1995, 10, 13, 5, 11078],
 [1995, 10, 14, 6, 8920],
 [1995, 10, 15, 7, 7996],
 [1995, 10, 16, 1, 10840],
 [1995, 10, 17, 2, 11974],
 [1995, 10, 18, 3, 11693],
 [1995, 10, 19, 4, 11463],
 [1995, 10, 20, 5, 11610],
 [1995, 10, 21, 6, 8673],
 [1995, 10, 22, 7, 7827],
 [1995, 10, 23, 1, 10770],
 [1995, 10, 24, 2, 11916],
 [1995, 10, 25, 3, 11573],
 [1995, 10, 26, 4, 11534],
 [1995, 10, 27, 5, 11449],
 [1995, 10, 28, 6, 8633],
 [1995, 10, 29, 7, 7876],
 [1995, 10, 30, 1, 10480],
 [1995, 10, 31, 2, 10740],
 [1995, 11, 1, 3, 11702],
 [1995, 11, 2, 4, 11746],
 [1995, 11, 3, 5, 11368],
 [1995, 11, 4, 6, 8438],
 [1995, 11, 5, 7, 7868],
 [1995, 11, 6, 1, 10809],
 [1995, 11, 7, 2, 12038],
 [1995, 11, 8, 3, 11702],
 [1995, 11, 9, 4, 11441],
 [1995, 11, 10, 5, 11246],
 [1995, 11, 11, 6, 8522],
 [1995, 11, 12, 7, 7891],
 [1995, 11, 13, 1, 10534],
 [1995, 11, 14, 2, 11455],
 [1995, 11, 15, 3, 11629],
 [1995, 11, 16, 4, 11436],
 [1995, 11, 17, 5, 11410],
 [1995, 11, 18, 6, 8493],
 [1995, 11, 19, 7, 7772],
 [1995, 11, 20, 1, 11476],
 [1995, 11, 21, 2, 12503],
 [1995, 11, 22, 3, 11304],
 [1995, 11, 23, 4, 7754],
 [1995, 11, 24, 5, 9125],
 [1995, 11, 25, 6, 8115],
 [1995, 11, 26, 7, 7500],
 [1995, 11, 27, 1, 10979],
 [1995, 11, 28, 2, 12002],
 [1995, 11, 29, 3, 11344],
 [1995, 11, 30, 4, 11215],
 [1995, 12, 1, 5, 11206],
 [1995, 12, 2, 6, 8429],
 [1995, 12, 3, 7, 7703],
 [1995, 12, 4, 1, 10346],
 [1995, 12, 5, 2, 11676],
 [1995, 12, 6, 3, 11188],
 [1995, 12, 7, 4, 11242],
 [1995, 12, 8, 5, 11166],
 [1995, 12, 9, 6, 8201],
 [1995, 12, 10, 7, 7595],
 [1995, 12, 11, 1, 10429],
 [1995, 12, 12, 2, 11784],
 [1995, 12, 13, 3, 11191],
 [1995, 12, 14, 4, 11403],
 [1995, 12, 15, 5, 11458],
 [1995, 12, 16, 6, 8509],
 [1995, 12, 17, 7, 7759],
 [1995, 12, 18, 1, 11139],
 [1995, 12, 19, 2, 12501],
 [1995, 12, 20, 3, 12043],
 [1995, 12, 21, 4, 11944],
 [1995, 12, 22, 5, 11204],
 [1995, 12, 23, 6, 8058],
 [1995, 12, 24, 7, 6999],
 [1995, 12, 25, 1, 7027],
 [1995, 12, 26, 2, 9447],
 [1995, 12, 27, 3, 11897],
 [1995, 12, 28, 4, 12530],
 [1995, 12, 29, 5, 12207],
 [1995, 12, 30, 6, 9093],
 [1995, 12, 31, 7, 7596],
 [1996, 1, 1, 1, 7683],
 [1996, 1, 2, 2, 9408],
 [1996, 1, 3, 3, 10954],
 [1996, 1, 4, 4, 11308],
 [1996, 1, 5, 5, 11631],
 [1996, 1, 6, 6, 8680],
 [1996, 1, 7, 7, 7735],
 [1996, 1, 8, 1, 10044],
 [1996, 1, 9, 2, 11018],
 [1996, 1, 10, 3, 11144],
 [1996, 1, 11, 4, 11304],
 [1996, 1, 12, 5, 11274],
 [1996, 1, 13, 6, 8488],
 [1996, 1, 14, 7, 7685],
 [1996, 1, 15, 1, 9912],
 [1996, 1, 16, 2, 11181],
 [1996, 1, 17, 3, 11148],
 [1996, 1, 18, 4, 11579],
 [1996, 1, 19, 5, 11292],
 [1996, 1, 20, 6, 8492],
 [1996, 1, 21, 7, 7701],
 [1996, 1, 22, 1, 10593],
 [1996, 1, 23, 2, 11451],
 [1996, 1, 24, 3, 11336],
 [1996, 1, 25, 4, 11405],
 [1996, 1, 26, 5, 11195],
 [1996, 1, 27, 6, 8487],
 [1996, 1, 28, 7, 7533],
 [1996, 1, 29, 1, 10374],
 [1996, 1, 30, 2, 11359],
 [1996, 1, 31, 3, 10889],
 [1996, 2, 1, 4, 11030],
 [1996, 2, 2, 5, 11335],
 [1996, 2, 3, 6, 8390],
 [1996, 2, 4, 7, 7531],
 [1996, 2, 5, 1, 10364],
 [1996, 2, 6, 2, 11360],
 [1996, 2, 7, 3, 11204],
 [1996, 2, 8, 4, 11529],
 [1996, 2, 9, 5, 11577],
 [1996, 2, 10, 6, 8578],
 [1996, 2, 11, 7, 7710],
 [1996, 2, 12, 1, 10542],
 [1996, 2, 13, 2, 11322],
 [1996, 2, 14, 3, 12094],
 [1996, 2, 15, 4, 11820],
 [1996, 2, 16, 5, 11666],
 [1996, 2, 17, 6, 8465],
 [1996, 2, 18, 7, 7763],
 [1996, 2, 19, 1, 10036],
 [1996, 2, 20, 2, 11598],
 [1996, 2, 21, 3, 11554],
 [1996, 2, 22, 4, 11697],
 [1996, 2, 23, 5, 11415],
 [1996, 2, 24, 6, 8692],
 [1996, 2, 25, 7, 7917],
 [1996, 2, 26, 1, 10693],
 [1996, 2, 27, 2, 11761],
 [1996, 2, 28, 3, 11428],
 [1996, 2, 29, 4, 10692],
 [1996, 3, 1, 5, 11785],
 [1996, 3, 2, 6, 8719],
 [1996, 3, 3, 7, 7885],
 [1996, 3, 4, 1, 10586],
 [1996, 3, 5, 2, 11475],
 [1996, 3, 6, 3, 11535],
 [1996, 3, 7, 4, 11446],
 [1996, 3, 8, 5, 11272],
 [1996, 3, 9, 6, 8611],
 [1996, 3, 10, 7, 7512],
 [1996, 3, 11, 1, 10668],
 [1996, 3, 12, 2, 11623],
 [1996, 3, 13, 3, 11338],
 [1996, 3, 14, 4, 11578],
 [1996, 3, 15, 5, 11860],
 [1996, 3, 16, 6, 8691],
 [1996, 3, 17, 7, 8010],
 [1996, 3, 18, 1, 10812],
 [1996, 3, 19, 2, 11764],
 [1996, 3, 20, 3, 11482],
 [1996, 3, 21, 4, 11653],
 [1996, 3, 22, 5, 11727],
 [1996, 3, 23, 6, 8534],
 [1996, 3, 24, 7, 8002],
 [1996, 3, 25, 1, 10662],
 [1996, 3, 26, 2, 11764],
 [1996, 3, 27, 3, 11532],
 [1996, 3, 28, 4, 11728],
 [1996, 3, 29, 5, 11659],
 [1996, 3, 30, 6, 8712],
 [1996, 3, 31, 7, 7956],
 [1996, 4, 1, 1, 10173],
 [1996, 4, 2, 2, 12055],
 [1996, 4, 3, 3, 11622],
 [1996, 4, 4, 4, 11881],
 [1996, 4, 5, 5, 10985],
 [1996, 4, 6, 6, 8354],
 [1996, 4, 7, 7, 7372],
 [1996, 4, 8, 1, 10659],
 [1996, 4, 9, 2, 11631],
 [1996, 4, 10, 3, 11429],
 [1996, 4, 11, 4, 11489],
 [1996, 4, 12, 5, 11462],
 [1996, 4, 13, 6, 8565],
 [1996, 4, 14, 7, 7687],
 [1996, 4, 15, 1, 10548],
 [1996, 4, 16, 2, 11754],
 [1996, 4, 17, 3, 11554],
 [1996, 4, 18, 4, 11282],
 [1996, 4, 19, 5, 11438],
 [1996, 4, 20, 6, 8451],
 [1996, 4, 21, 7, 7789],
 [1996, 4, 22, 1, 10957],
 [1996, 4, 23, 2, 11979],
 [1996, 4, 24, 3, 11342],
 [1996, 4, 25, 4, 11340],
 [1996, 4, 26, 5, 11070],
 [1996, 4, 27, 6, 8444],
 [1996, 4, 28, 7, 7567],
 [1996, 4, 29, 1, 10325],
 [1996, 4, 30, 2, 11391],
 [1996, 5, 1, 3, 11390],
 [1996, 5, 2, 4, 11397],
 [1996, 5, 3, 5, 11011],
 [1996, 5, 4, 6, 8483],
 [1996, 5, 5, 7, 7821],
 [1996, 5, 6, 1, 10585],
 [1996, 5, 7, 2, 11567],
 [1996, 5, 8, 3, 11403],
 [1996, 5, 9, 4, 11404],
 [1996, 5, 10, 5, 11471],
 [1996, 5, 11, 6, 8495],
 [1996, 5, 12, 7, 7758],
 [1996, 5, 13, 1, 10291],
 [1996, 5, 14, 2, 11757],
 [1996, 5, 15, 3, 11619],
 [1996, 5, 16, 4, 11637],
 [1996, 5, 17, 5, 11370],
 [1996, 5, 18, 6, 8696],
 [1996, 5, 19, 7, 7906],
 [1996, 5, 20, 1, 11073],
 [1996, 5, 21, 2, 11962],
 [1996, 5, 22, 3, 11733],
 [1996, 5, 23, 4, 11511],
 [1996, 5, 24, 5, 11835],
 [1996, 5, 25, 6, 8666],
 [1996, 5, 26, 7, 7746],
 [1996, 5, 27, 1, 8034],
 [1996, 5, 28, 2, 11151],
 [1996, 5, 29, 3, 12119],
 [1996, 5, 30, 4, 11964],
 [1996, 5, 31, 5, 11853],
 [1996, 6, 1, 6, 8866],
 [1996, 6, 2, 7, 7962],
 [1996, 6, 3, 1, 10916],
 [1996, 6, 4, 2, 11783],
 [1996, 6, 5, 3, 11695],
 [1996, 6, 6, 4, 11849],
 [1996, 6, 7, 5, 11750],
 [1996, 6, 8, 6, 8739],
 [1996, 6, 9, 7, 8013],
 [1996, 6, 10, 1, 10927],
 [1996, 6, 11, 2, 11978],
 [1996, 6, 12, 3, 11710],
 [1996, 6, 13, 4, 11521],
 [1996, 6, 14, 5, 11644],
 [1996, 6, 15, 6, 8783],
 [1996, 6, 16, 7, 8004],
 [1996, 6, 17, 1, 10981],
 [1996, 6, 18, 2, 12105],
 [1996, 6, 19, 3, 11779],
 [1996, 6, 20, 4, 12052],
 [1996, 6, 21, 5, 11759],
 [1996, 6, 22, 6, 8946],
 [1996, 6, 23, 7, 8128],
 [1996, 6, 24, 1, 11080],
 [1996, 6, 25, 2, 12150],
 [1996, 6, 26, 3, 12154],
 [1996, 6, 27, 4, 11957],
 [1996, 6, 28, 5, 12057],
 [1996, 6, 29, 6, 8956],
 [1996, 6, 30, 7, 8281],
 [1996, 7, 1, 1, 11779],
 [1996, 7, 2, 2, 13167],
 [1996, 7, 3, 3, 12563],
 [1996, 7, 4, 4, 9358],
 [1996, 7, 5, 5, 10823],
 [1996, 7, 6, 6, 9044],
 [1996, 7, 7, 7, 8248],
 [1996, 7, 8, 1, 11385],
 [1996, 7, 9, 2, 12623],
 [1996, 7, 10, 3, 12362],
 [1996, 7, 11, 4, 12256],
 [1996, 7, 12, 5, 11976],
 [1996, 7, 13, 6, 9152],
 [1996, 7, 14, 7, 8358],
 [1996, 7, 15, 1, 11421],
 [1996, 7, 16, 2, 12619],
 [1996, 7, 17, 3, 12660],
 [1996, 7, 18, 4, 12247],
 [1996, 7, 19, 5, 12049],
 [1996, 7, 20, 6, 9107],
 [1996, 7, 21, 7, 8349],
 [1996, 7, 22, 1, 11164],
 [1996, 7, 23, 2, 12731],
 [1996, 7, 24, 3, 12214],
 [1996, 7, 25, 4, 12307],
 [1996, 7, 26, 5, 12082],
 [1996, 7, 27, 6, 9012],
 [1996, 7, 28, 7, 8227],
 [1996, 7, 29, 1, 11232],
 [1996, 7, 30, 2, 12519],
 [1996, 7, 31, 3, 12128],
 [1996, 8, 1, 4, 12153],
 [1996, 8, 2, 5, 12088],
 [1996, 8, 3, 6, 9174],
 [1996, 8, 4, 7, 8327],
 [1996, 8, 5, 1, 11268],
 [1996, 8, 6, 2, 12508],
 [1996, 8, 7, 3, 12277],
 [1996, 8, 8, 4, 12385],
 [1996, 8, 9, 5, 12167],
 [1996, 8, 10, 6, 9175],
 [1996, 8, 11, 7, 8310],
 [1996, 8, 12, 1, 11499],
 [1996, 8, 13, 2, 12407],
 [1996, 8, 14, 3, 12294],
 [1996, 8, 15, 4, 12180],
 [1996, 8, 16, 5, 12419],
 [1996, 8, 17, 6, 9290],
 [1996, 8, 18, 7, 8305],
 [1996, 8, 19, 1, 11392],
 [1996, 8, 20, 2, 12270],
 [1996, 8, 21, 3, 12338],
 [1996, 8, 22, 4, 12291],
 [1996, 8, 23, 5, 12213],
 [1996, 8, 24, 6, 9130],
 [1996, 8, 25, 7, 8212],
 [1996, 8, 26, 1, 11201],
 [1996, 8, 27, 2, 12573],
 [1996, 8, 28, 3, 12339],
 [1996, 8, 29, 4, 12509],
 [1996, 8, 30, 5, 12479],
 [1996, 8, 31, 6, 9144],
 [1996, 9, 1, 7, 8250],
 [1996, 9, 2, 1, 8331],
 [1996, 9, 3, 2, 11506],
 [1996, 9, 4, 3, 12970],
 [1996, 9, 5, 4, 12657],
 [1996, 9, 6, 5, 12629],
 [1996, 9, 7, 6, 9396],
 [1996, 9, 8, 7, 8354],
 [1996, 9, 9, 1, 11543],
 [1996, 9, 10, 2, 12662],
 [1996, 9, 11, 3, 12420],
 [1996, 9, 12, 4, 12486],
 [1996, 9, 13, 5, 12019],
 [1996, 9, 14, 6, 9323],
 [1996, 9, 15, 7, 8561],
 [1996, 9, 16, 1, 12107],
 [1996, 9, 17, 2, 13063],
 [1996, 9, 18, 3, 12630],
 [1996, 9, 19, 4, 12535],
 [1996, 9, 20, 5, 12754],
 [1996, 9, 21, 6, 9492],
 [1996, 9, 22, 7, 8694],
 [1996, 9, 23, 1, 11605],
 [1996, 9, 24, 2, 12910],
 [1996, 9, 25, 3, 12768],
 [1996, 9, 26, 4, 12684],
 ...]
In [25]:
# Function Name: month_birth()
# This function will take a single required argument and 
# return a dict{} containing the total numbers of birth each month

def month_births(clean_data):
    births_per_month = {}
    for line in clean_data:
        months = line[1]
        births = line[4]
        
        if months in births_per_month:
            births_per_month[months] = births_per_month[months] + births
        else:
            births_per_month[months] = births
            
    return(births_per_month)

cdc_month_births = month_births(clean_data = cdc_list)
cdc_month_births
Out[25]:
{1: 3232517,
 2: 3018140,
 3: 3322069,
 4: 3185314,
 5: 3350907,
 6: 3296530,
 7: 3498783,
 8: 3525858,
 9: 3439698,
 10: 3378814,
 11: 3171647,
 12: 3301860}
In [26]:
# Function Name: dow_births()
# This function will take a single required argument as a input 
# and returns a dict{} containing the total number of births 
# for each unique value of the day_of_week

def dow_births(clean_data):
    
    births_per_day = {}
    
    for line in clean_data:
        day = line[3]
        births = line[4]
        
        if day in births_per_day:
            births_per_day[day] = births_per_day[day] + births
        else:
            births_per_day[day] = births
            
    return(births_per_day)

cdc_day_births = dow_births(clean_data = cdc_list)
cdc_day_births
Out[26]:
{1: 5789166,
 2: 6446196,
 3: 6322855,
 4: 6288429,
 5: 6233657,
 6: 4562111,
 7: 4079723}
In [27]:
# More general function: calc_counts() 
# This function will takes a two required parameters: clean_data-> A list of list, column-> the column number we  want to calculate the totals for

# Return the yearly totals for the dataset and assign the result to cdc_year_births.
# Return the monthly totals for the dataset and assign the result to cdc_month_births.
# Return the day-of-month totals for the dataset and assign the result to cdc_dom_births.
# Return the day-of-week totals for the dataset and assign the result to cdc_dow_births.

def calc_counts(clean_data, column):
    calc = {}
    
    for line in clean_data:
        columns = line[column]
        births = line[4]
        
        if columns in calc:
            calc[columns] = calc[columns] + births
        else:
            calc[columns] = births
            
    return(calc)

cdc_year_births = calc_counts(clean_data = cdc_list, column=0)
print('Return the yearly totals for the dataset and assign the result to cdc_year_births.')
cdc_year_births
Return the yearly totals for the dataset and assign the result to cdc_year_births.
Out[27]:
{1994: 3952767,
 1995: 3899589,
 1996: 3891494,
 1997: 3880894,
 1998: 3941553,
 1999: 3959417,
 2000: 4058814,
 2001: 4025933,
 2002: 4021726,
 2003: 4089950}
In [28]:
print('Return the monthly totals for the dataset and assign the result to cdc_month_births.')
cdc_month_births = calc_counts(clean_data = cdc_list, column=1)
cdc_month_births
Return the monthly totals for the dataset and assign the result to cdc_month_births.
Out[28]:
{1: 3232517,
 2: 3018140,
 3: 3322069,
 4: 3185314,
 5: 3350907,
 6: 3296530,
 7: 3498783,
 8: 3525858,
 9: 3439698,
 10: 3378814,
 11: 3171647,
 12: 3301860}
In [29]:
print('Return the day-of-month totals for the dataset and assign the result to cdc_dom_births.')
cdc_dom_births = calc_counts(clean_data = cdc_list, column=2)
cdc_dom_births
Return the day-of-month totals for the dataset and assign the result to cdc_dom_births.
Out[29]:
{1: 1276557,
 2: 1288739,
 3: 1304499,
 4: 1288154,
 5: 1299953,
 6: 1304474,
 7: 1310459,
 8: 1312297,
 9: 1303292,
 10: 1320764,
 11: 1314361,
 12: 1318437,
 13: 1277684,
 14: 1320153,
 15: 1319171,
 16: 1315192,
 17: 1324953,
 18: 1326855,
 19: 1318727,
 20: 1324821,
 21: 1322897,
 22: 1317381,
 23: 1293290,
 24: 1288083,
 25: 1272116,
 26: 1284796,
 27: 1294395,
 28: 1307685,
 29: 1223161,
 30: 1202095,
 31: 746696}
In [30]:
print('Return the day-of-week totals for the dataset and assign the result to cdc_dow_births.')
cdc_dow_births = calc_counts(clean_data = cdc_list, column=3)
cdc_dow_births
Return the day-of-week totals for the dataset and assign the result to cdc_dow_births.
Out[30]:
{1: 5789166,
 2: 6446196,
 3: 6322855,
 4: 6288429,
 5: 6233657,
 6: 4562111,
 7: 4079723}
In [32]:
# Function name: min_max
# This function will calculate the min and max values for dictionary thats passed in.

def min_max(myDict):
    import operator
    sorted_dict = sorted(myDict.items(),key=operator.itemgetter(1))
    
    min_max_dict = {}
    min_max_dict['min'] = sorted_dict[0]
    min_max_dict['max'] = sorted_dict[len(sorted_dict)-1]
    
    return(min_max_dict)

min_max_dow = min_max(cdc_year_births)
min_max_dow
Out[32]:
{'max': (2003, 4089950), 'min': (1997, 3880894)}
In [33]:
# Function name: getMinMaxYear()
# This function will calculate the min and max year for dictionary thats passed in.
# This function takes two required parameters: getList -> a list of lost, column: year column
def getMinMaxYear(getList, column):
    minMaxYear = []
    for item in getList:
        yearCol = item[column]
        if yearCol not in minMaxYear:
            minMaxYear.append(yearCol)
    
    finalMinMax={}
    finalMinMax['min'] = min(minMaxYear)
    finalMinMax['max'] = max(minMaxYear)
    
    return(finalMinMax)

# Function Name: getSat
# Problem Statement: how did the number of births on Saturday change each year between 1994 and 2003?

def getSat(getList,day):
    sat_count = {}
    for line in getList:
        if line[3]==day:
            if line[0] in sat_count:
                sat_count[line[0]] = sat_count[line[0]] + line[4]
            else:
                sat_count[line[0]] = line[4]
    
    #sorted_sat_count = sorted(sat_count.items(), key=lambda t: t[0])
    #sorted_sat_count1 = {}
    #for ni in sorted_sat_count:
        #sorted_sat_count1[ni[0]] = ni[1]
        
    yearMinMax = getMinMaxYear(getList,0)
    
    diff_sat = {}
    b=yearMinMax['min']
    for sat in sat_count:
        a = sat
        if b==yearMinMax['max']:
            b = sat + 1
        else:
            b = b
        aVal = sat_count[a]
        bVal = sat_count[b]
        diff_sat[sat] = bVal - aVal
    return(diff_sat)

sat_yrwise = getSat(getList = cdc_list, day=7)
sat_yrwise
Out[33]:
{1994: 0,
 1995: 2962,
 1996: 15416,
 1997: 24274,
 1998: 21623,
 1999: 26761,
 2000: 12298,
 2001: 31633,
 2002: 37377,
 2003: 35453}
In [ ]:
