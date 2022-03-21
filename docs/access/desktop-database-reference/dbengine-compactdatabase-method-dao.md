---
title: DBEngine.CompactDatabase Method (DAO)
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
ms.localizationpriority: high
ms.openlocfilehash: 2af07083b3421850e6aef988eb871821b11a8d27
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631614"
---
# <a name="dbenginecompactdatabase-method-dao"></a>DBEngine.CompactDatabase Method (DAO)

**S’applique à :** Access 2013 | Access 2016

Copie et compacte une base de données fermée et vous donne la possibilité de changer sa version, son ordre de tri et son chiffrement. (Espaces de travail Microsoft Access uniquement).

> [!NOTE]
> Lorsque vous utilisez les tableaux liés chiffrés pour une action, mise à jour et requêtes SQL [par exemple, une instruction SQL de mise à jour (CurrentDb.Execute « Mettre à jour... »)], vous devez fournir la clé de chiffrement. Par ailleurs, les tableaux liés sont limités à 19 caractères pour la clé de chiffrement. Voir la section **Tables liés chiffrés** à la fin de cette rubrique.

## <a name="syntax"></a>Syntaxe

*expression* .CompactDatabase(***SrcName** _, _*_DstName_*_, _*_DstLocale_*_, _*_Options_*_, _*_motdepasse_**)

*expression* Expression renvoyant un objet **DBEngine**.

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>SrcName</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Identifie une base de données existante et fermée. Il peut s'agir d'un nom de fichier et chemin d'accès complet, par exemple &quot;C:\db1.mdb&quot;. Si le nom de fichier possède une extension, vous devez la spécifier. Si votre réseau assure la prise en charge des chemins d'accès réseau, vous pouvez également préciser celui-ci, par exemple &quot;\\\\serveur1\partage1\rép1\db1.mdb&quot;</p></td>
</tr>
<tr class="even">
<td><p><em>DstName</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Nom de fichier (et chemin d'accès) de la base de données compactée que vous créez. Il est également possible de spécifier un chemin d'accès réseau. Vous ne pouvez pas utiliser cet argument pour indiquer le même fichier de base de données que NomSource.</p></td>
</tr>
<tr class="odd">
<td><p><em>DstLocale</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Expression en chaîne qui spécifie un ordre d’assemblage pour créer DstName, comme spécifié dans Remarques.</p>
<ul>
<li><p>Si vous omettez cet argument, les paramètres régionaux de DstName sont identiques à SrcName.</p></li>
<li><p>Vous pouvez également créer un mot de passe pour DstName par la concaténation de la chaîne de mot de passe (en commençant par &quot;;pwd=&quot;) avec une constante dans l'argument DstLocale, comme suit : dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</p></li>
<li><p>Pour utiliser le même argument DstLocale que SrcName (valeur par défaut) mais un nouveau mot de passe, entrez simplement une chaîne de mot de passe pour DstLocale: &quot;;pwd=NewPassword&quot;</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Facultatif. Constante ou combinaison de constantes qui indique une ou plusieurs options, comme indiqué dans la section Remarques. Vous pouvez combiner des options en associant les constantes correspondantes.</p></td>
</tr>
<tr class="odd">
<td><p><em>mot de passe</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Expression de chaîne contenant une clé de chiffrement, si la base de données est chiffrée. La chaîne &quot;; pwd =&quot; doit précéder le mot de passe réel. Si vous incluez un paramètre de mot de passe dans DstLocale, ce paramètre est ignoré.</p><p><strong>Remarque</strong>: il s’agit d’un paramètre obsolète et n’est pas pris en charge dans le format .ACCDB. Pour chiffrer un fichier .ACCDB, utilisez le « pwd = » option chaîne. Il est recommandé d'utiliser des mots de passe forts qui combinent des lettres majuscules et minuscules, des chiffres et des signes. Les mots de passe faibles ne regroupent pas ces éléments. Mot de passe fort : Y6dh!et5. Mot de passe faible : Maison27. Utilisez un mot de passe fort facile à mémoriser afin de ne pas avoir à le noter.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser l'une des constantes suivantes pour l'argument DstLocale afin de spécifier la propriété **CollatingOrder** du texte pour des comparaisons de chaînes.

<table>
<colgroup>
<col />
<col />
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


Vous pouvez utiliser l'une des constantes suivantes dans l'argument options pour spécifier s'il faut chiffrer ou déchiffrer la base de données pendant son compactage.

> [!NOTE]
> Les constantes dbEncrypt dbDecrypt sont déconseillées et sont pas prises en charge dans les formats de fichier .ACCDB.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
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


Si vous ne spécifiez pas de constante de chiffrement ou que vous incluez à la fois **dbDecrypt** et **dbEncrypt**, DstName aura le même chiffrement que SrcName.

Vous pouvez utiliser l'une des constantes suivantes dans l'argument options pour spécifier la version du format de données de la base de données compactée. Cette constante n'affecte que la version du format des données de NomDest mais non la version des objets définis par Microsoft Access, tels que les formulaires et les états.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
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
<td><p>Crée une base de données qui utilise le format fichier version 12.0 de moteur de base de données Microsoft Access pendant le compactage.</p></td>
</tr>
</tbody>
</table>


Vous ne pouvez spécifier qu'une seule constante de version. Si vous l'omettez, NomDest aura la même version que NomSource. Vous ne pouvez compacter NomDest que dans une version identique ou supérieure à celle de NomSource.

À mesure que vous modifiez les données dans une base de données, le fichier de base de données peut se fragmenter et utiliser plus d'espace disque que nécessaire. Vous pouvez périodiquement utiliser la méthode **CompactDatabase** pour compacter la base de données et défragmenter le fichier de base de données. La base compactée est généralement plus petite et s'exécute plus rapidement. Il est également possible de modifier l'ordre de classement, le chiffrement et la version du format de données pendant la copie et le compactage de la base de données.

Vous devez fermer NomSource avant de la compacter. Dans un environnement multi-utilisateur, les autres utilisateurs ne peuvent avoir NomSource ouverte pendant que vous la compactez. Si NomSource n'est pas fermée ou n'est pas accessible en mode exclusif, une erreur se produit.

Dans la mesure où **CompactDatabase** crée une copie de la base de données, vous devez avoir suffisamment d'espace disque pour la base de données d'origine et la base dupliquée. L'opération de compactage échoue si il n'y a pas suffisamment d'espace disque. La base de données dupliquée NomDest ne doit pas nécessairement être sur le même disque que NomSource. Après le compactage réussi d'une base de données, vous pouvez supprimer le fichier NomSource et renommer le fichier NomDest compacté avec le nom du fichier d'origine.

La méthode **CompactDatabase** copie toutes les données et les options d'autorisation de sécurité de la base de données spécifiée par SrcName vers la base de données spécifiée par DstName.

> [!NOTE]
> Étant donné que la méthode **CompactDatabase** ne convertit pas les objets Microsoft Access, vous ne devez pas utiliser **CompactDatabase** pour convertir une base de données contenant ces objets.

## <a name="encrypted-linked-tables"></a>Tableaux liés chiffrés

Les mots de passe chiffrés dépendent du format de fichiers de la base de données que vous utilisez. Si vous utilisez une base de données Access 2003 (.mdb) ou antérieure, vous aurez un mot de passe pour protéger la base de données et un mot de passe distinct pour chiffrer la base de données. Pour les bases de données Access 2007 (.accdb) et version ultérieure (.mdb), la seule option consiste à chiffrer et protéger la base de données avec un mot de passe, comme l’option deux mots de passe distincts a été supprimée.

> [!NOTE]
> Pour les bases de données Access 2007 (.accdb), le mot de passe est la clé de chiffrement

Vous pouvez utiliser l’exemple suivant du code VBA pour un bouton de commande :

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


Exemple de code suivant montre comment utiliser CompactDatabase avec un mot de passe (clé de chiffrement) et créer un lien à un tableau dans cette base de données compactée. Notez qu’un mot de passe doit être fourni.

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
