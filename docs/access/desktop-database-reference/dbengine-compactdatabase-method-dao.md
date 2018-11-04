---
title: Méthode DBEngine.CompactDatabase (DAO)
TOCTitle: CompactDatabase Method
ms:assetid: 03f3a156-005a-4b71-81b0-598f326f7d42
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844821(v=office.15)
ms:contentKeyID: 48542997
ms.date: 10/24/2016
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052936
f1_categories:
- Office.Version=v15
ms.openlocfilehash: df7533376bf6f6d3c5387173a90c7d5e1a5013cd
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950046"
---
# <a name="dbenginecompactdatabase-method-dao"></a>Méthode DBEngine.CompactDatabase (DAO)

**S’applique à**: Access 2013 | Accès 2016

Copie et compacte une base de données fermée et vous donne la possibilité de changer sa version, l’ordre de classement et le chiffrement. (Espaces de travail Microsoft Access uniquement).

> [!NOTE]
> Lors de l’utilisation de tables liées chiffrées pour action, mise à jour et les requêtes SQL [par exemple une instruction SQL UPDATE (« Mise à jour … » CurrentDb.Execute)], vous devez fournir la clé de chiffrement. En outre, les tables liées sont limités à 19 caractères pour la clé de chiffrement. Consultez la section **Encrypted des tables liées** à la fin de cette rubrique.

## <a name="syntax"></a>Syntaxe

*expression* . CompactDatabase (***NomSource***, ***NomDest***, ***ParamètresRégionauxDst***, ***Options***, ***le mot de passe***)

*expression* Expression qui renvoie un objet **DBEngine** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Obligatoire/Facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>NomSource</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Chaîne</strong></p></td>
<td><p>Identifie une base de données existante et fermée. Il peut être un chemin d’accès complet et le nom de fichier, tel que &quot;C:\db1.mdb&quot;. Si le nom de fichier doté d’une extension, vous devez le spécifier. Si votre réseau prend en charge, vous pouvez également spécifier un chemin d’accès réseau, tel que &quot; \\server1\share1\dir1\db1.mdb&quot;</p></td>
</tr>
<tr class="even">
<td><p><em>NomDest</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Chaîne</strong></p></td>
<td><p>nom de fichier (et chemin d’accès) de la base de données compactée que vous créez. Vous pouvez également spécifier un chemin d’accès réseau. Vous ne pouvez pas utiliser cet argument pour spécifier le même fichier de base de données que NomSource.</p></td>
</tr>
<tr class="odd">
<td><p><em>ParamètresRégionauxDst</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>Expression de chaîne qui indique un ordre de classement pour la création de NomDest, de la façon décrite dans la section Remarques.</p>
<ul>
<li><p>Si vous omettez cet argument, les paramètres régionaux de NomDest et NomSource seront identiques.</p></li>
<li><p>Vous pouvez également créer un mot de passe pour NomDest par la concaténation de la chaîne de mot de passe (commençant par &quot;; pwd =&quot;) avec une constante dans l’argument ParamètresRégionauxDst, comme suit : dbLangSpanish &amp; &quot;; pwd = NewPassword&quot;.</p></li>
<li><p>Si vous souhaitez utiliser le même argument ParamètresRégionauxDst que NomSource (valeur par défaut), mais un nouveau mot de passe, entrez simplement une chaîne de mot de passe pour ParamètresRégionauxDst : &quot;; pwd = NewPassword&quot;</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>Facultatif. Constante ou combinaison de constantes qui indique une ou plusieurs options, comme indiqué dans la section Remarques. Vous pouvez combiner des options en associant les constantes correspondantes.</p></td>
</tr>
<tr class="odd">
<td><p><em>mot de passe</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>Expression chaîne contenant une clé de chiffrement, si la base de données est chiffrée. La chaîne &quot;; pwd =&quot; doivent précéder le mot de passe. Si vous incluez un paramètre de mot de passe dans ParamètresRégionauxDst, ce paramètre est ignoré.</p><p><strong>Remarque</strong>: il s’agit du paramètre désapprouvé et n’est pas pris en charge. Format de fichier ACCDB. Pour chiffrer une. Fichier ACCDB, utilisez le « pwd = « chaîne d’option. [!REMARQUE] Définissez des mots de passe forts qui combinent des lettres minuscules et majuscules, des nombres et des symboles. Les mots de passe faibles ne regroupent pas ces éléments. Mot de passe fort : Y6dh!et5. Mot de passe faible : Maison27. Utilisez un mot de passe fort dont vous pouvez vous souvenir sans devoir le noter.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser l'une des constantes suivantes pour l'argument ParamètresRégionauxDst afin de définir la propriété **CollatingOrder** pour des comparaisons de chaînes de texte.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Ordre de classement</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbLangGeneral</strong></p></td>
<td><p>Anglais, allemand, français, portugais, italien et espagnol</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangArabic</strong></p></td>
<td><p>Arabe</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangChineseSimplified</strong></p></td>
<td><p>Chinois simplifié</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangChineseTraditional</strong></p></td>
<td><p>Chinois traditionnel</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangCyrillic</strong></p></td>
<td><p>Russe</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangCzech</strong></p></td>
<td><p>Tchèque</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangDutch</strong></p></td>
<td><p>Néerlandais</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangGreek</strong></p></td>
<td><p>Grec</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangHebrew</strong></p></td>
<td><p>Hébreu</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangHungarian</strong></p></td>
<td><p>Hongrois</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangIcelandic</strong></p></td>
<td><p>Islandais</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangJapanese</strong></p></td>
<td><p>Japonais</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangKorean</strong></p></td>
<td><p>Coréen</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangNordic</strong></p></td>
<td><p>Langues nordiques (Moteur de base de données Microsoft Jet version 1.0 uniquement)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangNorwDan</strong></p></td>
<td><p>Norvégien et danois</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangPolish</strong></p></td>
<td><p>Polonais</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSlovenian</strong></p></td>
<td><p>Slovène</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangSpanish</strong></p></td>
<td><p>Espagnol traditionnel</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSwedFin</strong></p></td>
<td><p>Suédois et finnois</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangThai</strong></p></td>
<td><p>Thaï</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangTurkish</strong></p></td>
<td><p>Turc</p></td>
</tr>
</tbody>
</table>

<br/>

Vous pouvez utiliser l'une des constantes suivantes dans l'argument options pour spécifier s'il faut chiffrer ou déchiffrer la base de données pendant son compactage.

> [!NOTE]
> Les constantes dbEncrypt dbDecrypt déconseillée et sont pas pris en charge. Formats de fichier ACCDB.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbEncrypt</strong></p></td>
<td><p>Chiffre la base de données pendant le compactage.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDecrypt</strong></p></td>
<td><p>Déchiffre la base de données pendant le compactage.</p></td>
</tr>
</tbody>
</table>

<br/>

Si vous omettez la constante de chiffrement ou que vous incluez à la fois **dbDecrypt** et **dbEncrypt**, NomDest aura le même chiffrement que NomSource.

Vous pouvez utiliser l'une des constantes suivantes dans l'argument options pour spécifier la version du format de données de la base de données compactée. Cette constante n'affecte que la version du format des données de NomDest mais non la version des objets définis par Microsoft Access, tels que les formulaires et les états.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbVersion10</strong></p></td>
<td><p>Crée une base de données qui utilise le format de fichier de la version 1.0 du moteur de base de données Microsoft Jet pendant le compactage.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>Crée une base de données qui utilise le format de fichier de la version 1.1 du moteur de base de données Microsoft Jet pendant le compactage.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>Crée une base de données qui utilise le format de fichier de la version 2.0 du moteur de base de données Microsoft Jet pendant le compactage.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>Crée une base de données qui utilise le format de fichier de la version 3.0 (compatible avec la version 3.5) du moteur de base de données Microsoft Jet pendant le compactage.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>Crée une base de données qui utilise le format de fichier de la version 4.0 du moteur de base de données Microsoft Jet pendant le compactage.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>Crée une base de données qui utilise le format de fichier de la version 12.0 du moteur de base de données Microsoft Access pendant le compactage.</p></td>
</tr>
</tbody>
</table>

<br/>

Vous ne pouvez spécifier qu'une seule constante de version. Si vous omettez, NomDest aura la même version que NomSource. Vous pouvez compacter NomDest que dans une version est la même ou version ultérieure à celle de NomSource.

À mesure que vous modifiez les données dans une base de données, le fichier de base de données peut se fragmenter et utiliser plus d'espace disque que nécessaire. Vous pouvez périodiquement utiliser la méthode **CompactDatabase** pour compacter la base de données et défragmenter le fichier de base de données. La base compactée est généralement plus petite et s'exécute plus rapidement. Il est également possible de modifier l'ordre de classement, le chiffrement et la version du format de données pendant la copie et le compactage de la base de données.

Vous devez fermer NomSource avant de la compacter. Dans un environnement multi-utilisateurs, les autres utilisateurs ne peuvent pas avoir NomSource ouverte pendant que vous la compactez. Si NomSource n’est pas fermée ou n’est pas disponible pour une utilisation exclusive, une erreur se produit.

Dans la mesure où **CompactDatabase** crée une copie de la base de données, vous devez avoir suffisamment d'espace disque pour la base de données d'origine et la base dupliquée. L'opération de compactage échoue si il n'y a pas suffisamment d'espace disque. La base de données dupliquée NomDest ne doit se trouver sur le même disque que NomSource. Après le compactage réussi d’une base de données, vous pouvez supprimer le fichier NomSource et renommer le fichier NomDest compacté au nom du fichier d’origine.

La méthode **CompactDatabase** copie toutes les données et les paramètres d’autorisation de sécurité à partir de la base de données spécifiée par NomSource vers la base de données spécifiée par NomDest.

> [!NOTE]
> [!REMARQUE] Comme la méthode **CompactDatabase** ne convertit pas les objets Microsoft Access, vous ne devez pas utiliser **CompactDatabase** pour convertir une base de données contenant de tels objets.

## <a name="encrypted-linked-tables"></a>Tables liées chiffrés

Les mots de passe chiffrés dépendent de la base de données que vous utilisez le format de fichier. Si vous utilisez un Access 2003 (.mdb) ou une base de données antérieure, vous aurez un mot de passe pour protéger la base de données et un mot de passe distinct pour crypter la base de données. Pour Access 2007 (.accdb) et version ultérieure bases de données (.mdb), la seule option consiste à chiffrer et protéger la base de données avec un mot de passe, comme l’option pour que les deux mots de passe a été supprimée.

> [!NOTE]
> Pour les bases de données Access 2007 (.accdb), le mot de passe est la clé de chiffrement

Vous pouvez utiliser l’exemple de code VBA suivant pour un bouton de commande :

```vb
    Private Sub Command0_Click()
    
    Dim strSourcePath As String
    Dim strDestPath As String
    
    strSourcePath = "<path>\sourceDb.accdb"
    strDestPath = "<path>\destDb.accdb"
    
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
    
    Set CurrentDatabase = CurrentDb
    Set LinkedTableDef = CurrentDatabase.CreateTableDef 
    ("My Linked Table")
    LinkedTableDef.Connect = "MS Access;pwd=Access";database=" & strDestPath
    LinkedTableDef.RefreshLink
    
    
    MsgBox "Finished"
    
    End Sub 
```

<br/>

L’exemple de code suivant montre comment utiliser CompactDatabase avec un mot de passe (clé de chiffrement), puis lier à une table dans cette base de données compactée. Notez que le mot de passe doit être fourni.

```vb
    Private Sub CompactAndLink_Click() 
     
    Dim strSourcePath As String
    Dim strDestPath As String
    Dim strSourceTableName As String
    Dim strDestTableName As String
    Dim tdf As TableDef
     
    strSourcePath = "<path>\<database>.accdb"
    strDestPath = "<path>\<database>.accdb"
    strSourceTableName = "<table name in destination database>"
    strDestTableName = "<linked table name>"
     
    ' Compact source database into new destination database with encrypted password
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
     
    ' Link to one of the tables in the destination database
    ' Password must be provided in the Connect property
     
    Set CurrentDatabase = CurrentDb
    Set tdf = CurrentDatabase.CreateTableDef(strDestTableName)
       
        With tdf
            .Connect = ";pwd=Access" & ";DATABASE=" & strDestPath
            .SourceTableName = strSourceTableName
        End With
        
    CurrentDatabase.TableDefs.Append tdf
     
    MsgBox "Database compacted and encrypted password applied. Link to table also completed."
     
    End Sub
```
