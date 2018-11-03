---
title: Initialisation du pilote de Source de données texte
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
ms.openlocfilehash: f87c8e45cbc719ee50c017abd45a8950dc6ec7ed
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945445"
---
# <a name="initializing-the-text-data-source-driver"></a>Initialisation du pilote de Source de données texte


**S’applique à**: Access 2013, Office 2013


Le même pilote de base de données est utilisé pour les sources de type Données de texte et HTML.

Lorsque vous installez le pilote de base de données de Source de données texte, le programme d’installation écrit un ensemble de valeurs par défaut dans les sous-clés et ISAM Formats du Registre Microsoft Windows. Vous ne devez pas modifier ces paramètres directement. Utilisez le programme d’installation pour votre application pour ajouter, supprimer ou modifier ces paramètres. Les sections suivantes décrivent l’initialisation et les paramètres de Format ISAM pour le pilote de base de données de Source de données de texte.

## <a name="text-data-source-initialization-settings"></a>Paramètres d'initialisation de source de données de texte

Le **Access Connectivity Engine\\Formats ISAM\\dossier texte** inclut les paramètres d’initialisation du pilote Acetxt.dll, utilisé pour l’accès externe aux fichiers de données de texte. L'exemple ci-dessous montre des paramètres par défaut pour les entrées de ce dossier.

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

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
<td><p>Win32</p></td>
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
<td><p>Jeu de caractères</p></td>
<td><p>Indicateur du mode de stockage des pages. Les valeurs suivantes peuvent être utilisées :</p>
<p></p>
<ul>
<li><p>ANSI — page de code ANSI de la machine. Conversions AnsiToUnicode et UnicodeToAnsi réalisées.</p></li>
<li><p>OEM — page de code OEM de la machine. Conversions OEMToUnicode et UnicodeToOEM réalisées.</p></li>
<li><p>Unicode   — conversions de page de code non réalisées.</p></li>
<li><p>&lt;nombre décimal&gt; — le numéro de page de code d’un jeu de caractères spécifique. Conversions de Unicode et seront effectuées.</p></li>
</ul>
<p></p>
<p>La valeur par défaut est ANSI. Les valeurs sont de type REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>Format</p></td>
<td><p>Peut être un des suivants : TabDelimited, CSVDelimited, délimité (&lt;caractère&gt;). Le délimiteur à caractère unique dans le format délimité peut être n’importe quel caractère unique à l’exception des guillemets doubles (&quot;). La valeur par défaut est CSVDelimited. Les valeurs sont de type REG_SZ.</p></td>
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


## <a name="text-data-source-isam-formats"></a>Formats ISAM de source de données Texte

Le **Access Connectivity Engine\\Formats ISAM\\texte** dossier contient les entrées suivantes.

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
<td><p>Engine</p></td>
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
> <P>Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.</P>



## <a name="html-import-isam-formats"></a>Formats ISAM d'importation HTML

Le **Access Connectivity Engine\\Formats ISAM\\importation HTML** dossier contient les entrées suivantes.

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
<td><p>Engine</p></td>
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
> <P>Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.</P>



## <a name="html-export-isam-formats"></a>Formats ISAM d'exportation HTML

Le **Access Connectivity Engine\\Formats ISAM\\exportation HTML** dossier contient les entrées suivantes.

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
<td><p>Engine</p></td>
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
> <P>Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.</P>



## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a>Personnalisation du fichier schema.ini pour données Texte et HTML

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
<td><p>Peut être définie sur une des valeurs suivantes : TabDelimited, CSVDelimited, délimité (&lt;caractère&gt;), ou FixedLength. Le délimiteur spécifié pour le format de fichier délimité peut être n’importe quel caractère unique à l’exception des guillemets doubles (&quot;).</p></td>
</tr>
<tr class="odd">
<td><p>FormatFixe</p></td>
<td><p>Utilisé uniquement lorsque le format est FixedLength, peut être défini avec l'une des valeurs suivantes : RaggedEdge ou TrueFixedLength.
 RaggedEdge permet aux lignes d'être terminées par une marque de fin de paragraphe (caractère de retour chariot). TrueFixedLength nécessite que chaque ligne comporte un nombre exact de caractères. Tous les caractères de retour chariot qui ne se situent pas à une limite de ligne sont considérées comme intégrés dans un champ. Si ce paramètre n'est pas présent, la valeur par défaut est RaggedEdge.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Indique le nombre de lignes à analyser lors de l'estimation des types de données des colonnes. La valeur 0 indique que la recherche est effectuée dans l'ensemble du fichier.</p></td>
</tr>
<tr class="odd">
<td><p>Jeu de caractères</p></td>
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
<td><p>Peut être définie à une des valeurs suivantes : symbole monétaire en préfixe, sans séparation ($1) symbole monétaire en suffixe, sans séparation (1$) symbole monétaire en préfixe avec un caractère séparation ($ 1) symbole monétaire en suffixe avec une séparation d’un caractère (1 $) si cette entrée est absent, la valeur par défaut dans le panneau de configuration de Windows est utilisée.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyDigits</p></td>
<td><p>Définit le nombre de chiffres utilisés pour la partie décimale d'un montant monétaire. Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyNegFormat</p></td>
<td><p>Peut être une des valeurs suivantes : ($1) : $1 – 1 $ $1 – (1$) – 1$ $ 1 – $ 1 – – 1 $ – 1 1 $ $– $ 1 – $ 1 – 1 – $ ($ 1) (1 $) le signe dollar est indiqué à des fins de cet exemple, mais elle doit être remplacée par la valeur CurrencySymbol appropriée dans le programme. Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</p></td>
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
<td><p>Col1, Col2, …</p></td>
<td><p>Répertorie les colonnes dans le fichier texte à lire. Le format de cette entrée doit être : <em>Coln</em>=<em>NomColonne</em> type [Width <em> #</em>] <em>NomColonne</em>: les noms de colonne contenant des espaces doivent être placés entre guillemets. <em>type</em>: peut être Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime. Binaire, OLE, texte ou Mémo. En outre, les types de pilote texte ODBC suivants sont pris en charge : Char (comme texte) Float (comme Double) Integer (comme court) LongChar (comme Mémo) Date <em>format de date</em> dans le cas d’un type Mémo un marqueur de format supplémentaire [Attribute Hyperlink] peut être permet de spécifier les colonnes qui doivent être des URL actifs dans Microsoft Access. Dans le cas d'un type Décimal, les marqueurs de format supplémentaires [Scale #] Precision #] doivent être utilisés.</p></td>
</tr>
<tr class="odd">
<td><p>DélimiteurTexte</p></td>
<td><p>Peut être tout caractère utilisé pour délimiter les chaînes qui contiennent un des autres caractères spéciaux.
 Ex. : &quot;ABC&quot;,&quot;xyz, pqr&quot;,&quot;hij&quot; si cette entrée n’est pas présente le séparateur par défaut est un guillemet double. Si cette entrée est la chaîne &quot;aucun&quot; puis aucun des caractères ne sont considérés comme des séparateurs.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!REMARQUE] Lorsque vous modifiez des paramètres Schema.ini, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.


