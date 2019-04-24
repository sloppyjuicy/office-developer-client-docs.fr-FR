---
title: Utilisation des jeux d'enregistrements
TOCTitle: Working with Recordsets
ms:assetid: 9cd52866-2738-8150-381c-eee0b8a6cd36
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249711(v=office.15)
ms:contentKeyID: 48546608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d4b877b680c80a10067e19065facd4ce9e4819d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305971"
---
# <a name="working-with-recordsets"></a>Utilisation de recordsets

**S’applique à** : Access 2013, Office 2013 

L'objet **Recordset** possède des fonctionnalités intégrées permettant de réorganiser l'ordre des données dans le jeu de résultats, ce qui permet, d'une part, de rechercher des enregistrements spécifiques sur base de critères définis et, d'autre part, d'optimiser ces opérations de recherche à l'aide d'index. La disponibilité de ces fonctionnalités dépend du fournisseur et, dans certains cas, notamment celui de la propriété [Index](index-property-ado.md), de la structure même de la source de données.

## <a name="arranging-data"></a>Organisation des données

En règle générale, le moyen le plus efficace d'organiser les données d'un objet **Recordset** consiste à spécifier une clause ORDER BY dans la commande SQL utilisée pour retourner les résultats dans le jeu d'enregistrements. Gardez néanmoins à l'esprit que vous devrez parfois modifier l'ordre des données dans un objet **Recordset** lorsqu'il a déjà été créé. En définissant la propriété **Sort**, vous êtes en mesure d'établir l'ordre dans lequel les lignes d'un objet **Recordset** seront parcourues. En outre, la propriété **Filter** permet de déterminer les lignes accessibles lors du parcours des lignes.

La propriété **Sort** définit ou renvoie une valeur de type **String** indiquant les noms des champs de l'objet **Recordset** qui feront l'objet du tri. Chaque nom est séparé par une virgule et peut être suivi d'un espace et du mot clé **ASC** (pour un tri par ordre croissant) ou **DESC** (pour un tri par ordre décroissant). Par défaut, si aucun mot clé n'est spécifié, le champ sera trié par ordre croissant.

L'efficacité de l'opération de tri réside dans le fait que les données ne sont pas triées physiquement, mais simplement accédées dans l'ordre spécifié par un index.

Lorsque vous utilisez la propriété **Sort**, la propriété [CursorLocation](cursorlocation-property-ado.md) doit être définie avec la valeur **adUseClient**. En l'absence d'un index existant, un index temporaire sera créé pour chaque champ spécifié dans la propriété **Sort**.

Si vous définissez une chaîne vide comme valeur de la propriété **Sort**, les lignes sont rétablies dans leur ordre initial et les index temporaires sont supprimés. En revanche, les index existants seront conservés.

Supposons qu’un objet **Recordset** contienne trois champs nommés *firstName*, *middleInitial* et *lastName*. Définissez la propriété **sort** sur la chaîne «», qui triera l' **objet Recordset** par nom de famille dans l'ordre décroissant, puis par prénom par ordre croissant. L'initiale du second prénom sera ignorée.

Aucun champ référencé dans une chaîne de critères de tri ne peut être nommé « ASC » ou « DESC », car ces noms provoquent des conflits avec les mots clés **ASC** et **DESC**. Attribuez au nom du champ posant problème un alias à l'aide du mot clé **AS** dans la requête qui retourne l'objet **Recordset**.

Pour plus d'informations sur le filtrage des objets **Recordset**, consultez la section Filtrage des résultats, plus loin dans cette rubrique.

## <a name="finding-a-specific-record"></a>Recherche d'un enregistrement spécifique

Les méthodes ADO [Find](find-method-ado.md) et [Seek](seek-method-ado.md) permettent de localiser un enregistrement spécifique dans un objet **Recordset**. La méthode **Find** est prise en charge par un grand nombre de fournisseurs, mais est limitée à un seul critère de recherche. La méthode **Seek** permet une recherche basée sur plusieurs critères, mais n'est pas prise en charge par tous les fournisseurs.

Des champs indexés permettent d'améliorer considérablement les performances de la méthode **Find** ainsi que des propriétés **Sort** et **Filter** d'un objet **Recordset**. Vous pouvez créer un index interne pour un objet **Field** en définissant sa propriété dynamique [Optimize](optimize-property-dynamic-ado.md). Cette propriété dynamique s'ajoute à la collection **Properties** de l'objet **Field** lorsque vous affectez à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient**. Gardez à l'esprit qu'il s'agit d'un index interne d'ADO, ce qui signifie que vous ne pouvez y accéder ou l'utiliser à d'autres fins. En outre, sachez que cet index est différent de la propriété **Index** de l'objet [Recordset](index-property-ado.md).

La méthode **Find** permet de localiser rapidement une valeur dans une colonne (champ) d'un objet **Recordset**. Vous pouvez généralement accélérer l'exécution de la méthode **Find** sur une colonne en utilisant la propriété **Optimize** pour y créer un index.

La méthode **Find** limite votre recherche au contenu d'un seul champ. Quant à la méthode **Seek**, elle requiert la présence d'un index et présente également d'autres limitations. Si vous devez lancer une recherche sur plusieurs champs non indexés ou si votre fournisseur ne prend pas les index en charge, vous pouvez limiter les résultats en utilisant la propriété **Filter** de l'objet **Recordset**.

### <a name="find"></a>Find

La méthode **Find** recherche, dans un objet **Recordset**, une ligne répondant à un critère spécifié. Le cas échéant, il est également possible de définir la direction de la recherche, la ligne de départ et le décalage depuis la ligne de début. Si une ligne correspond au critère défini, la position de la ligne active est définie sur l'enregistrement trouvé. Dans le cas contraire, la position active est définie sur la fin (ou le début) de l'objet **Recordset**, selon la direction de la recherche.

Seul un nom de colonne unique peut être spécifié comme critère. En effet, cette méthode ne prend pas en charge les recherches sur plusieurs colonnes.

L'opérateur de comparaison du critère peut être «**\>**» (supérieur à), «**\<**» (inférieur à), «=» (égal à),\>«=» (supérieur ou égal à),\<«=» (inférieur ou égal à),\<\>«» (différent de) ou «like» (critères spéciaux).

La valeur du critère doit être une chaîne, un nombre à virgule flottante ou une date. Les valeurs de chaîne sont délimitées par des\#guillemets simples ou des signes «» (dièse) (par exemple, «State = 'wa' \#»\#ou «state = WA»). les valeurs de Date sont délimitées par des signes «\#» (dièse) (par exemple\_, \> \#«\#date de début 7/22/97»).

Si l'opérateur de comparaison est « like », la valeur de la chaîne peut contenir un astérisque (\*) pour rechercher une ou plusieurs occurrences d'un caractère ou d'une sous-chaîne. Par exemple, « state like 'M\*' » correspond à Maine et Massachusetts. Vous pouvez également utiliser des astérisques au début et à la fin pour rechercher une sous-chaîne dans les valeurs. Par exemple, « state like '\*as\* » correspond à Alaska, Arkansas et Massachusetts.

Les astérisques ne peuvent être utilisés qu'à la fin d'une chaîne de critère ou au début et à la fin d'une chaîne de critère, comme nous l'avons vu dans les exemples précédents. L'utilisation d'un astérisque comme caractère générique de début ('\*str') ou comme caractère générique incorporé ('s\*r') provoque une erreur.

### <a name="seek-and-index"></a>Seek et Index

Il est conseillé d’utiliser conjointement la méthode **Seek** avec la propriété **Index** si le fournisseur sous-jacent prend les index en charge sur l’objet **Recordset**. La méthode [Supports](supports-method-ado.md)**(adSeek)** permet de déterminer si le fournisseur sous-jacent prend **Seek** en charge, et la méthode **Supports(adIndex)** de déterminer si les index sont pris en charge par le fournisseur. (Par exemple, le [fournisseur OLE DB pour Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) prend **Seek** et **Index** en charge.)

Si la méthode **Seek** ne trouve pas la ligne recherchée, aucune erreur n'est générée et la ligne est positionnée à la fin du **Recordset**. Veillez à définir la propriété **Index** sur l'index souhaité avant d'exécuter cette méthode.

Cette méthode n'est prise en charge qu'avec des curseurs côté serveur. La méthode Seek n'est pas prise en charge lorsque la valeur de la propriété **CursorLocation** de l'objet [Recordset](cursorlocation-property-ado.md) est **adUseClient**.

Cette méthode peut être utilisée dans le seul cas où l'objet **Recordset** a été ouvert avec la valeur [adCmdTableDirect](commandtypeenum.md) de **CommandTypeEnum**.

## <a name="filtering-the-results"></a>Filtrage des résultats

La méthode **Find** limite votre recherche au contenu d'un seul champ. La méthode **Seek** exige la présence d'un index et possède également d'autres limitations.Si vous devez exécuter une recherche sur plusieurs champs non indexés ou si votre fournisseur ne prend pas les index en charge, vous pouvez limiter vos résultats en utilisant la propriété **Filter** de l'objet **Recordset**.

La propriété **Filtre** permet d'effectuer une recherche sélective d'enregistrements dans un objet **Recordset**. L'objet **Recordset** filtré devient le curseur actif. En d'autres termes, les enregistrements qui ne répondent pas aux critères de la propriété **Filter** ne sont pas disponibles dans l'objet **Recordset** tant que la propriété **Filter** n'est pas supprimée. Les autres propriétés qui renvoient des valeurs relatives au curseur actif sont également affectées, par exemple **AbsolutePosition**, **AbsolutePage**, **RecordCount** et **PageCount**. Ceci s'explique par le fait que l'affectation d'une valeur spécifique à la propriété **Filter** déplace la position d'enregistrement actif au niveau du premier enregistrement qui correspond à la nouvelle valeur.

La propriété **Filter** prend un argument de type Variant. Cette valeur représente l'une des trois méthodes d'utilisation de la propriété **Filter**: une chaîne de critères, une constante **FilterGroupEnum** ou un tableau de signets. Pour plus d'informations, consultez les sections Filtrage à l'aide d'une chaîne de critères, Filtrage avec une constante et Filtrage avec des signets, plus loin dans cette rubrique.

> [!NOTE]
> [!REMARQUE] Lorsque vous connaissez les données à sélectionner, il est généralement plus efficace d'ouvrir un **Recordset** avec une instruction SQL capable de filtrer efficacement le jeu de résultats au lieu d'utiliser la propriété **Filter**.

Pour supprimer un filtre d'un **Recordset**, utilisez la constante **adFilterNone**. En définissant une chaîne vide ("") comme valeur de la propriété **Filter**, vous obtenez le même résultat qu'en utilisant la constante **adFilterNone**.

### <a name="filtering-with-a-criteria-string"></a>Filtrage à l'aide d'une chaîne de critères

La chaîne de critères est composée de clauses de type *NomChamp opérateur valeur* (par exemple, «LastName = 'Smith'»). Vous pouvez créer des clauses composées en concaténant des clauses individuelles avec AND (par exemple, "LastName = 'Smith'et FirstName = 'John'") et ou (par exemple,). Vous pouvez créer des clauses composées en concaténant des clauses individuelles avec AND (par exemple, "LastName = 'Smith'AND FirstName = 'John'") et ou (par exemple, "LastName = 'Smith'ou LastName = 'Jones'"). Lorsque vous utilisez des chaînes de critères, gardez les points suivants à l’esprit :

- *NomChamp* doit être un nom de champ valide du **Recordset**. Si le nom de champ contient des espaces, vous devez le mettre entre crochets.

- *L'opérateur* doit être l'un des suivants \<: \>, \<, = \>, = \< \>,, = ou like.

- *Value* est la valeur avec laquelle comparer les valeurs des champs (par exemple, 'Smith', \#8/24/95\#, 12,345 ou $50,00). Utilisez des guillemets simples (') avec des chaînes et des\#signes dièse () avec des dates. Pour les nombres, vous pouvez utiliser les points décimaux, le signe dollar et les notations scientifiques. Si la valeur du champ *Opérateur* est LIKE, celle du champ *Valeur* peut utiliser des caractères génériques. Uniquement l'astérisque (\*) et le signe de pourcentage (%) les caractères génériques sont autorisés et ils doivent être le dernier caractère de la chaîne. La *valeur* doit être différente de Null.
    
  > [!NOTE]
  > Pour inclure des guillemets simples (’) dans le filtre *Valeur*, utilisez deux guillemets simples pour en afficher un seul. Par exemple, pour filtrer la valeur *O'Malley*, la chaîne de critères doit être «col1 = 'O' 'Malley'». 
  > 
  > Pour inclure des guillemets simples au début et à la fin de la valeur du filtre, placez des signes dièse (#) de part et d'autre de la chaîne. Par exemple, pour filtrer sur *«1»*, la chaîne de critères doit être «col1 = # ' 1 ' #».

Il n'existe pas de priorité entre AND et OR. Les clauses peuvent être regroupées dans des parenthèses. Notez toutefois que vous ne pouvez pas regrouper des clauses jointes par OR, puis associer le groupe à une autre clause avec AND, comme ceci :

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

Le filtre doit être construit comme suit :

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

Dans une clause LIKE, vous pouvez utiliser un caractère générique au début et à la fin de la chaîne (par exemple, LastName\*like\*'mit') ou uniquement à la fin du modèle (par exemple,) ou à la fin du modèle (par exemple, LastName like'Smit\*').

### <a name="filtering-with-a-constant"></a>Filtrage avec une constante

Les constantes suivantes sont disponibles pour le filtrage des objets **Recordset**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFilterAffectedRecords</strong></p></td>
<td><p>Affiche uniquement les enregistrements concernés par le dernier appel à <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong> ou <strong>CancelBatch</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterConflictingRecords</strong></p></td>
<td><p>Affiche les enregistrements pour lesquels la dernière mise à jour par lot a échoué.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterFetchedRecords</strong></p></td>
<td><p>Affiche les enregistrements du cache actif , c'est-à-dire les résultats du dernier appel visant à extraire des enregistrements de la base de données.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterNone</strong></p></td>
<td><p>Supprime le filtre actif et restaure l'affichage de tous les enregistrements.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterPendingRecords</strong></p></td>
<td><p>Affiche uniquement les enregistrements qui ont été modifiés mais pas encore envoyés au serveur. Applicable uniquement pour le mode de mise à jour par lot.</p></td>
</tr>
</tbody>
</table>

<br/>

Les constantes de filtre simplifient la résolution des conflits d'enregistrements individuels pendant le mode de mise à jour par lot en vous permettant de n'afficher, par exemple, que les enregistrements affectés par le dernier appel de la méthode **UpdateBatch**, comme illustré dans l'exemple suivant :

```vb 
 
'BeginDeleteGroup 
    'add some bogus records 
    With objRs1 
        For i = 0 To 8 
            .AddNew 
            .Fields("CompanyName") = "Shipper Number " & i + 1 
            .Fields("Phone") = "(425) 555-000" & (i + 1) 
            .Update 
        Next i 
         
    're-connect & update 
        .ActiveConnection = GetNewConnection 
        .UpdateBatch 
         
    'filter on newly added records 
        .Filter = adFilterAffectedRecords 
        Debug.Print "Deleting the " & .RecordCount & _ 
                    " records you just added." 
         
    'delete the newly added bogus records 
        .Delete adAffectGroup 
        .Filter = adFilterNone 
        Debug.Print .RecordCount & " records remain." 
         
        .Close 
    End With 
'EndDeleteGroup 
```

### <a name="filtering-with-bookmarks"></a>Filtrage à l'aide de signets

Enfin, vous pouvez transmettre un tableau de signets de type Variant à la propriété **Filter**. Le curseur résultant contiendra uniquement les enregistrements dont le signet a été transmis à la propriété. L'exemple de code suivant permet de créer un tableau de signets à partir des enregistrements d'un objet **Recordset** dont le nom contient la lettre « B » (dans le champ *ProductName*). Il passe ensuite le tableau à la propriété **Filter** et affiche les informations de l'objet **Recordset** filtré qui en résulte.

```vb 
 
'BeginFilterBkmk 
    Dim vBkmkArray() As Variant 
    Dim i As Integer 
 
    'Recordset created using "SELECT * FROM Products" as command. 
    'So, we will check to see if ProductName has a capital B, and 
    'if so, add to the array. 
    i = 0 
    Do While Not objRs.EOF 
        If InStr(1, objRs("ProductName"), "B") Then 
            ReDim Preserve vBkmkArray(i) 
            vBkmkArray(i) = objRs.Bookmark 
            i = i + 1 
            Debug.Print objRs("ProductName") 
        End If 
        objRs.MoveNext 
    Loop 
     
    'Filter using the array of bookmarks. 
    objRs.Filter = vBkmkArray 
     
    objRs.MoveFirst 
    Do While Not objRs.EOF 
        Debug.Print objRs("ProductName") 
        objRs.MoveNext 
    Loop 
    'EndFilterBkmk 
```

## <a name="creating-a-clone-of-a-recordset"></a>Création d'un clone d'un jeu d'enregistrements

Utilisez la méthode **Clone** pour créer plusieurs objets **Recordset** dupliqués, notamment dans le cas où vous souhaitez conserver plusieurs enregistrements actifs dans un jeu d'enregistrements donné. La méthode **Clone** est plus efficace que la technique qui consiste à créer et ouvrir un nouvel objet **Recordset** avec une définition identique à celle de l'original.

L'enregistrement actif d'un clone créé est initialement le premier enregistrement. Le pointeur de l'enregistrement actif dans un objet **Recordset** cloné n'est pas synchronisé avec l'original et vice versa. Vous pouvez naviguer de façon indépendante dans chaque objet **Recordset**.

Les modifications apportées à un objet **Recordset** apparaissent dans tous ses clones, quel que soit le type de curseur utilisé. Toutefois, après l'exécution de la méthode [Requery](requery-method-ado.md) sur l'objet **Recordset** d'origine, les clones ne sont plus synchronisés avec l'original.

La fermeture de l'objet **Recordset** d'origine ne ferme pas ses copies pas plus que la fermeture d'une copie ne ferme l'objet d'origine ni aucune autre copie.

Vous pouvez cloner un objet **Recordset** uniquement s'il prend en charge les signets. Les valeurs des signets sont interchangeables ; en d'autres termes, une référence de signet d'un objet **Recordset** donné fait référence au même enregistrement dans chacun de ses clones.

