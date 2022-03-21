---
title: QueryDef. Connecter property (DAO)
TOCTitle: Connect Property
ms:assetid: 14f19205-e92e-acc6-5677-b6d88772d5da
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845479(v=office.15)
ms:contentKeyID: 48543398
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bad4a18e5bb80dac53053542d69aba71af2e11c6
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634183"
---
# <a name="querydefconnect-property-dao"></a>QueryDef. Connecter property (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui fournit des informations sur la source de base de données dans une requête SQL directe. Type **String** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* .Connect

*expression* Variable représentant un objet **QueryDef**.

## <a name="remarks"></a>Remarques

Le **Connect** paramètre de la propriété est un **chaîne** composé d’un spécificateur de type base de données et de zéro ou plusieurs paramètres séparés par des points-virgules. Le **Connect** propriété transmet des informations supplémentaires à ODBC et certains pilotes ISAM selon vos besoins.

Pour exécuter une requête SQL directe sur une table liée à votre fichier de base de données Microsoft Access, vous devez d'abord affecter une chaîne de connexion ODBC valide à la propriété **Connect** de la base de données de la table liée.

Le chemin présenté dans le tableau suivant représente le chemin complet du répertoire contenant les fichiers de base de données ; il doit être précédé par l'identificateur DATABASE=. Dans certains cas (comme avec Microsoft Excel et les bases de données avec moteur de base de données Microsoft Access), vous devez inclure un nom de fichier spécifique à l'argument du chemin de la base de données.

Le tableau suivant indique les types de base de données possible et leur spécificateurs de base de données correspondantes et les chemins d’accès relatifs le **Connect** paramètre de la propriété.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Type de base de données</p></th>
<th><p>Spécificateur</p></th>
<th><p>Exemple</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Base de données Microsoft Access</p></td>
<td><p>[database];</p></td>
<td><p>drive:\path\filename</p></td>
</tr>
<tr class="even">
<td><p>dBase III</p></td>
<td><p>dBase III</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="odd">
<td><p>dBase IV</p></td>
<td><p>dBase IV</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="even">
<td><p>dBase 5</p></td>
<td><p>dBase 5.0</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 3.x</p></td>
<td><p>Paradox 3.x</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="even">
<td><p>Paradox 4.x</p></td>
<td><p>Paradox 4.x</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 5.x</p></td>
<td><p>Paradox 5.x</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel</p></td>
<td><p>Excel 3.0 ;</p></td>
<td><p>drive:\path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel</p></td>
<td><p>Excel 4.0;</p></td>
<td><p>drive:\path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 5.0 ou Microsoft Excel 95</p></td>
<td><p>Excel 5.0 ;</p></td>
<td><p>drive:\path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 97</p></td>
<td><p>Excel</p></td>
<td><p>drive:\path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WKS et WK1</p></td>
<td><p>Lotus WK1 ;</p></td>
<td><p>drive:\path\filename.wk1</p></td>
</tr>
<tr class="odd">
<td><p>WK3 Lotus 1-2-3</p></td>
<td><p>Lotus WK3 ;</p></td>
<td><p>drive:\path\filename.wk3</p></td>
</tr>
<tr class="even">
<td><p>WK4 Lotus 1-2-3</p></td>
<td><p>Lotus WK4 ;</p></td>
<td><p>drive:\path\filename.wk4</p></td>
</tr>
<tr class="odd">
<td><p>Importation HTML</p></td>
<td><p>Importation HTML ;</p></td>
<td><p>drive:\path\filename</p></td>
</tr>
<tr class="even">
<td><p>Exportation HTML</p></td>
<td><p>Exportation HTML ;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="odd">
<td><p>Texte</p></td>
<td><p>Text;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="even">
<td><p>ODBC</p></td>
<td><p>ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</p></td>
<td><p>Aucun</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Exchange</p></td>
<td><p>Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</p></td>
<td><p>drive:\path\filename</p></td>
</tr>
</tbody>
</table>


Si le spécificateur est uniquement "ODBC;", le pilote ODBC affiche une boîte de dialogue répertoriant tous les noms des sources de données ODBC enregistrées pour permettre à l'utilisateur de sélectionner une base de données.

Si un mot de passe est requis sans être fourni dans le **Connect** propriété définissant, une boîte de dialogue Connexion s’affiche la première fois une table est accessible par le pilote ODBC puis de nouveau si la connexion est fermée et rouvert.

Pour les données dans Microsoft Exchange, la clé MAPILEVEL obligatoire doit être définie avec un chemin de dossier entièrement résolu (par exemple, « Mailbox – Pat SmithIAlpha/Today »). Le chemin n'inclut pas le nom du dossier qui sera ouvert comme une table ; au lieu de cela, le nom du dossier doit être spécifié comme argument nom de la méthode **CreateTable**. La clé TABLETYPE doit avoir la valeur « 0 » pour ouvrir un dossier (par défaut) ou « 1 » pour ouvrir un carnet d'adresses. La clé PROFILE prend la valeur par défaut du profil en cours d'utilisation.

Dans un objet **QueryDef** d'un espace de travail Microsoft Access, vous pouvez utiliser la propriété **Connect** avec la propriété ReturnsRecords afin de créer une requête SQL directe ODBC. L’argument type_base_données de la chaîne de connexion correspond à "ODBC;" et la chaîne contient ensuite des informations spécifiques du pilote ODBC servant à accéder aux données distantes. Pour plus d'informations, consultez la documentation relative au pilote.

> [!NOTE]
> - Vous devez définir la **Connect** propriété avant de définir la **ReturnsRecords** propriété.
> - Vous devez disposer des autorisations d’accès à l’ordinateur qui contient le serveur de base de données que vous essayez d’accéder.


