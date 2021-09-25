---
title: Initialisation du pilote de source de données texte
TOCTitle: Initializing the Text Data Source driver
ms:assetid: cba0864e-5f94-bf43-4708-b1981e3acaff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834391(v=office.15)
ms:contentKeyID: 48547718
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032166
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 9fbe8bcde259f69086c511ec0343d345a15aa425
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594089"
---
# <a name="initializing-the-text-data-source-driver"></a>Initialisation du pilote de source de données texte

**S’applique à** : Access 2013, Office 2013

Le même pilote de base de données est utilisé à la fois pour les sources de données texte et pour les sources de données HTML.

Lorsque vous installez le pilote de base de données textuelle source de données, le programme d’installation écrit un ensemble de valeurs par défaut dans le Registre Microsoft Windows dans les sous-clés Engines et ISAM Formats. Vous ne devez pas modifier ces paramètres directement ; utilisez le programme d’installation de votre application pour ajouter, supprimer ou modifier ces paramètres. Les sections suivantes décrivent l’initialisation et les paramètres de format ISAM pour le pilote de base de données de source de données texte.

## <a name="text-data-source-initialization-settings"></a>Paramètres d’initialisation de la source de données texte

Le dossier Texte des **\\ formats ISAM \\** du moteur de connectivité Access inclut les paramètres d’initialisation du pilote Acetxt.dll, utilisé pour l’accès externe aux fichiers de données texte. L'exemple ci-dessous montre des paramètres par défaut pour les entrées de ce dossier.

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

<br/>

Le moteur de base de données Microsoft Access utilise les entrées de dossier Text suivantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Entrée</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>win32</p></td>
<td><p>Emplacement de Acetxt.dll. Le Chemin d'accès complet est déterminé au moment de l'installation. Les valeurs sont de type REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Nombre de lignes devant être analysées pour déterminer les types de colonne. En présence de la valeur 0, la recherche porte sur le fichier entier. La valeur par défaut est 25. Les valeurs sont de type REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Valeur binaire indiquant si la première ligne de la table contient des noms de colonnes. La valeur 01 indique que les noms de colonne sont pris dans la première ligne, pendant l'importation.</p></td>
</tr>
<tr class="even">
<td><p>CharacterSet</p></td>
<td><p>Indicateur du mode de stockage des pages. Les valeurs suivantes peuvent être utilisées :</p>
<p></p>
<ul>
<li><p>ANSI — page de code ANSI de la machine. Conversions AnsiToUnicode et UnicodeToAnsi réalisées.</p></li>
<li><p>OEM — page de code OEM de la machine. Conversions OEMToUnicode et UnicodeToOEM réalisées.</p></li>
<li><p>Unicode   — conversions de page de code non réalisées.</p></li>
<li><p>&lt;nombre décimal &gt; — Numéro de page de code d’un jeu de caractères spécifique. Les conversions à partir de et vers Unicode sont réalisées.</p></li>
</ul>
<p></p>
<p>La valeur par défaut est ANSI. Les valeurs sont de type REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>Format</p></td>
<td><p>Peut être l’une des suivantes : TabDelimited, CSVDelimited, Delimited ( &lt; caractère unique &gt; ). Le délimiteur à caractère unique au format délimité peut être n’importe quel caractère unique à l’exception d’un guillemet double ( &quot; ). Le format par défaut est CSVDelimited. Les valeurs sont de type REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>Extensions</p></td>
<td><p>Extension de tout fichier à parcourir lorsque vous recherchez des données textuelles. Les extensions par défaut sont txt, csv, tab, asc. Les valeurs sont de type REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>ExportCurrencySymbols</p></td>
<td><p>Valeur binaire qui indique si le symbole monétaire correspondant est inclus lorsque les champs monétaires sont exportées. La valeur 01 indique que le symbole est inclus. La valeur 00 indique que seules les données numériques sont exportées. La valeur par défaut est 01. Les valeurs sont de type REG_BINARY.</p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a>Formats ISAM de source de données texte

Le **dossier Texte \\ formats \\ ISAM** du moteur de connectivité Access contient les entrées suivantes.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom d'entrée</p></th>
<th><p>Type</p></th>
<th><p>Valeur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Moteur</p></td>
<td><p>REG_SZ</p></td>
<td><p>Texte</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Fichier texte (*.txt; *.csv; *.tab; *.asc)</p></td>
</tr>
<tr class="odd">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Fichiers texte (*.txt; *.csv; *.tab; *.asc)</p></td>
</tr>
<tr class="even">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="odd">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="odd">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextImport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Permet d'importer des données du fichier externe dans la base de données active. La modification des données dans la base de données active n'entraîne pas celle des données du fichier externe.</p></td>
</tr>
<tr class="even">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Permet de créer, dans la base de données active, une table liée au fichier externe. La modification des données dans la base de données active entraîne celle des données dans le fichier externe.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Permet d'exporter les données de la base de données active vers le fichier texte. Ce processus entraîne l'écrasement des données si l'exportation a lieu vers un fichier existant.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.

## <a name="html-import-isam-formats"></a>Formats ISAM d’importation HTML

Le **dossier d’importation HTML des \\ formats ISAM \\** du moteur de connectivité Access contient les entrées suivantes.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom d'entrée</p></th>
<th><p>Type</p></th>
<th><p>Valeur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Moteur</p></td>
<td><p>REG_SZ</p></td>
<td><p>Texte</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Fichiers HTML (*.ht*)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>ResultTextImport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Permet d'importer des données du fichier externe dans la base de données active. La modification des données dans la base de données active n'entraîne pas celle des données du fichier externe.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Permet de créer, dans la base de données active, une table liée au fichier externe. La modification des données dans la base de données active entraîne celle des données dans le fichier externe.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.

## <a name="html-export-isam-formats"></a>Formats ISAM d’exportation HTML

Le **dossier d’exportation HTML des \\ formats ISAM \\** du moteur de connectivité Access contient les entrées suivantes.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom d'entrée</p></th>
<th><p>Type</p></th>
<th><p>Valeur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Moteur</p></td>
<td><p>REG_SZ</p></td>
<td><p>Texte</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Fichiers HTML (*.htm)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Permet d'exporter les données de la base de données active vers le fichier texte. Ce processus entraîne l'écrasement des données si l'exportation a lieu vers un fichier existant.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a>Personnalisation du fichier Schema.ini pour le texte et les données HTML

Pour lire, importer ou exporter des données de texte et des données HTML, vous devez créer un fichier Schema.ini en plus d'inclure les informations ISAM de texte dans le fichier .ini. Le fichier Schema.ini contient les paramètres spécifiques d'une source de données : mise en forme du fichier de texte, lecture du fichier lors de l'importation et format d'exportation par défaut des fichiers. Les exemple suivants montrent la disposition pour un fichier de largeur fixe, Filename.txt :

```text
    [Filename.txt] 
    
    ColNameHeader=False 
    
    Format=FixedLength 
    
    FixedFormat= RaggedEdge 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    Col1=columnname Char Width 24 
    
    Col2=columnname2 Date Width 9 
    
    Col3=columnname7 Float Width 10 
    
    Col4=columnname8 Integer Width 10 
    Col5=columnname9 LongChar Width 10
```

<br/>

De même, la mise en forme d'un fichier délimité est définie comme suit :

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

<br/>

Si vous exportez des données dans un fichier de texte délimité, définissez également la mise en forme de ce fichier :

```text
    [Export: My Special Export] 
    
    ColNameHeader=True 
    
    Format=TabDelimited 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    DateTimeFormat=mm.dd.yy.hh.mm.ss 
    
    CurrencySymbol=Dm 
    
    CurrencyPosFormat=0 
    
    CurrencyDigits=2 
    
    CurrencyNegFormat=0 
    
    CurrencyThousandSymbol=, 
    
    CurrencyDecimalSymbol=. 
    
    DecimalSymbol=, 
    
    NumberDigits=2 
    
    NumberLeadingZeros=0 
    
    TextDelimeter="
```

<br/>

L'exemple My Special Export fait référence à une option d'exportation spécifique ; vous pouvez combiner d'autres options d'exportation au moment de la connexion. Ce dernier exemple correspond à un nom de source de données (DSN) pouvant être passé au moment de la connexion (facultatif). Les trois sections de format peuvent être incluses dans le même fichier .ini..

Le moteur de base de données Microsoft Access utilise les entrées du fichier Schema.ini suivantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Entrée</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ColNameHeader</p></td>
<td><p>Peut être défini à l'aide des valeurs <strong>True</strong> (le premier enregistrement contient les noms de colonne) ou <strong>False</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Format</p></td>
<td><p>Peut être définie sur l’une des valeurs suivantes : TabDelimited, CSVDelimited, Delimited ( &lt; caractère unique ) ou &gt; FixedLength. Le délimiteur spécifié pour le format de fichier délimité peut être n’importe quel caractère unique à l’exception d’un guillemet double ( &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>FixedFormat</p></td>
<td><p>Utilisé uniquement lorsque le format est FixedLength, peut être défini avec l'une des valeurs suivantes : RaggedEdge ou TrueFixedLength. RaggedEdge permet aux lignes d'être terminées par une marque de fin de paragraphe (caractère de retour chariot). TrueFixedLength nécessite que chaque ligne comporte un nombre exact de caractères. Tous les caractères de retour chariot qui ne se situent pas à une limite de ligne sont considérées comme intégrés dans un champ. Si ce paramètre n'est pas présent, la valeur par défaut est RaggedEdge.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Indique le nombre de lignes à analyser lors de l'estimation des types de données des colonnes. La valeur 0 indique que la recherche est effectuée dans l'ensemble du fichier.</p></td>
</tr>
<tr class="odd">
<td><p>CharacterSet</p></td>
<td><p>Peut être défini en OEM, ANSI, UNICODE ou le nombre décimal d'une page de code valide, et indique le jeu de caractères du fichier source.</p></td>
</tr>
<tr class="even">
<td><p>DateTimeFormat</p></td>
<td><p>Peut être défini en une chaîne de format indiquant les dates et les heures. Cette entrée doit être spécifiée si tous les champs date/heure de l'importation/exportation sont traités avec le même format. Tous les formats de moteur de base de données Microsoft Jet à l'exception d'AM et PM sont pris en charge. En l'absence d'une chaîne de format, les options de représentation de date et d'heure courtes du Panneau de configuration de Windows sont utilisées.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencySymbol</p></td>
<td><p>Indique le symbole à utiliser pour les valeurs monétaires dans le fichier de texte ($ ou €, par exemple). Si cette entrée n'est pas présente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyPosFormat</p></td>
<td><p>Vous pouvez définir l’une des valeurs suivantes : Préfixe de symbole monétaire sans suffixe de symbole monétaire de séparation ($1) sans préfixe de symbole monétaire (1$) avec un suffixe de symbole monétaire avec séparation d’un caractère (1 $) Si cette entrée est absente, la valeur par défaut du Panneau de contrôle Windows est utilisée.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyDigits</p></td>
<td><p>Définit le nombre de chiffres utilisés pour la partie décimale d'un montant monétaire. Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyNegFormat</p></td>
<td><p>Peut être l’une des valeurs suivantes : ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) Le signe dollar est affiché aux fins de cet exemple, mais il doit être remplacé par la valeur CurrencySymbol appropriée dans le programme réel. Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyThousandSymbol</p></td>
<td><p>Désigne le symbole mono-caractère à utiliser pour séparer les milliers dans les valeurs monétaires du fichier de texte. Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyDecimalSymbol</p></td>
<td><p>Peut être tout caractère utilisé pour séparer la partie entière et la partie décimale d'un montant monétaire. Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</p></td>
</tr>
<tr class="odd">
<td><p>DecimalSymbol</p></td>
<td><p>Peut être tout caractère utilisé pour séparer la partie entière et la partie décimale d'un nombre. Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</p></td>
</tr>
<tr class="even">
<td><p>NumberDigits</p></td>
<td><p>Indique le nombre de chiffres utilisées dans la partie décimale d'un nombre. Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</p></td>
</tr>
<tr class="odd">
<td><p>NumberLeadingZeros</p></td>
<td><p>Indique si une valeur décimale inférieure à 1 et supérieure à –1 doit commencer par des zéros. Cette valeur peut être False (pas de zéros) ou True.</p></td>
</tr>
<tr class="even">
<td><p>Col1, Col2, ...</p></td>
<td><p>Répertorie les colonnes à lire dans le fichier de texte. Le format de cette entrée doit être : <em>Coln</em> = <em>columnName</em> type [Width ] columnName : les noms de colonnes avec des espaces incorporés doivent être entre <em>#</em> guillemets. <em></em> <em>type</em>: peut être Bit, Octets, Court, Long, Décimal, Monétaire, Simple, Double, Date/Heure. Binaire, OLE, Texte ou Mémo. En outre, les types de pilotes de texte ODBC suivants sont pris en charge : Char (identique à Text) Float (identique à Double) Integer (identique à Short) LongChar (identique à Mémo) Format de <em>date</em> dans le cas d’un type Mémo, un marqueur de format supplémentaire [Lien hypertexte d’attribut] peut être utilisé pour spécifier des colonnes qui doivent être des URL actives dans Microsoft Access. Dans le cas d'un type Décimal, les marqueurs de format supplémentaires [Scale #] Precision #] doivent être utilisés.</p></td>
</tr>
<tr class="odd">
<td><p>TextDelimiter</p></td>
<td><p>Peut être tout caractère utilisé pour délimiter les chaînes qui contiennent un des autres caractères spéciaux. Par exemple, &quot;abc &quot; , &quot; xyz,pqr , hij Si cette entrée n’est pas présente, le délimiteur par défaut &quot; est un &quot; &quot; guillemet double. Si cette entrée est la chaîne aucun, aucun caractère ne sera traité comme &quot; &quot; des délimiteur.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!REMARQUE] Lorsque vous modifiez des paramètres Schema.ini, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.


