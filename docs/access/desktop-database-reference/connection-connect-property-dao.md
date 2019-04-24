---
title: Connection. Connect, propriété (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e44ce5b4acf58f3f9d9e887d0136baed64c8e227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295925"
---
# <a name="connectionconnect-property-dao"></a>Connection. Connect, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui fournit des informations sur la source d'une connexion ouverte. Type de données **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*expression* . Connexions

*expression* Variable qui représente un objet **Connection** .

## <a name="remarks"></a>Remarques

Le paramètre de la propriété **Connect** est un type **String** composé d'un spécificateur de type de base de données et de zéro ou plusieurs paramètres séparés par des points-virgules. La propriété **Connect** passe des informations complémentaires à ODBC et à certains pilotes ISAM selon les circonstances.

Pour exécuter une requête SQL directe sur une table liée au fichier de base de données Microsoft Access, vous devez d'abord définir la propriété **Connect** de la base de données de la table liée sur une chaîne de connexion ODBC valide.

Dans le cas d'un objet **TableDef** représentant une table liée, la valeur de la propriété **Connect** est constituée d'un ou de deux éléments (un spécificateur de type de base de données et un chemin d'accès à la base de données), se terminant chacun par un point-virgule.

Le chemin présenté dans le tableau suivant représente le chemin complet du répertoire contenant les fichiers de base de données ; il doit être précédé par l'identificateur DATABASE=. Dans certains cas (comme avec Microsoft Excel et les bases de données avec moteur de base de données Microsoft Access), vous devez inclure un nom de fichier spécifique à l'argument du chemin de la base de données.

Le tableau suivant indique les types de bases de données possibles, ainsi que leurs spécificateurs et chemins correspondants, pour la valeur de la propriété **Connect**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td><p>[base de données];</p></td>
<td><p>lecteur: \ chemin\nom_fichier</p></td>
</tr>
<tr class="even">
<td><p>dBASE III</p></td>
<td><p>dBASE III;</p></td>
<td><p>lecteur: \ chemin d'accès</p></td>
</tr>
<tr class="odd">
<td><p>dBASE IV</p></td>
<td><p>dBASE IV;</p></td>
<td><p>lecteur: \ chemin d'accès</p></td>
</tr>
<tr class="even">
<td><p>dBASE 5</p></td>
<td><p>dBASE 5.0;</p></td>
<td><p>lecteur: \ chemin d'accès</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 3.x</p></td>
<td><p>Paradox 3.x;</p></td>
<td><p>lecteur: \ chemin d'accès</p></td>
</tr>
<tr class="even">
<td><p>Paradox 4.x</p></td>
<td><p>Paradox 4.x;</p></td>
<td><p>lecteur: \ chemin d'accès</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 5.x</p></td>
<td><p>Paradox 5.x;</p></td>
<td><p>lecteur: \ chemin d'accès</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 3.0</p></td>
<td><p>Excel 3.0;</p></td>
<td><p>lecteur: \ path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 4.0</p></td>
<td><p>Excel 4.0;</p></td>
<td><p>lecteur: \ path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 5.0 ou Microsoft Excel 95</p></td>
<td><p>Excel 5.0;</p></td>
<td><p>lecteur: \ path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 97</p></td>
<td><p>Excel 8.0;</p></td>
<td><p>lecteur: \ path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WKS et WK1</p></td>
<td><p>Lotus WK1;</p></td>
<td><p>lecteur: \ path\filename.WK1</p></td>
</tr>
<tr class="odd">
<td><p>Lotus 1-2-3 WK3</p></td>
<td><p>Lotus WK3;</p></td>
<td><p>lecteur: \ path\filename.WK3</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WK4</p></td>
<td><p>Lotus WK4;</p></td>
<td><p>lecteur: \ path\filename.WK4</p></td>
</tr>
<tr class="odd">
<td><p>Importation HTML</p></td>
<td><p>HTML Import;</p></td>
<td><p>lecteur: \ chemin\nom_fichier</p></td>
</tr>
<tr class="even">
<td><p>Exportation HTML</p></td>
<td><p>Export HTML;</p></td>
<td><p>lecteur: \ chemin d'accès</p></td>
</tr>
<tr class="odd">
<td><p>Texte</p></td>
<td><p>Textes</p></td>
<td><p>lecteur: \ chemin d'accès</p></td>
</tr>
<tr class="even">
<td><p>ODBC</p></td>
<td><p>ODBC BASE de données = base de données; UID = utilisateur; PWD = mot de passe; DSN = DataSourceName; [LOGINTIMEOUT = secondes;]</p></td>
<td><p>Aucun</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Exchange</p></td>
<td><p>Exchange 4,0; MAPILEVEL = folderPath; [TABLETYPE = {0 | 1}]; [PROFILe = profil;] [PWD = mot de passe;] [Base de données = base de données;]</p></td>
<td><p>lecteur: \ chemin\nom_fichier</p></td>
</tr>
</tbody>
</table>


Si le spécificateur est uniquement "ODBC;", le pilote ODBC affiche une boîte de dialogue répertoriant tous les noms des sources de données ODBC enregistrées pour permettre à l'utilisateur de sélectionner une base de données.

Si un mot de passe est obligatoire et qu'il n'est pas fourni par la propriété **Connect**, une boîte de dialogue de connexion s'affiche la première fois que le pilote ODBC accède à une table et une nouvelle fois si la connexion est fermée et rouverte.

Pour les données dans Microsoft Exchange, la clé MAPILEVEL obligatoire doit être définie avec un chemin de dossier entièrement résolu (par exemple, « Mailbox - Pat SmithIAlpha/Today »). Le chemin d'accès n'inclut pas le nom du dossier qui sera ouvert en tant que table; le nom de ce dossier doit plutôt être spécifié en tant qu'argument nom de la méthode **CreateTable** . La clé TABLETYPE doit avoir la valeur « 0 » pour ouvrir un dossier (par défaut) ou « 1 » pour ouvrir un carnet d'adresses. La clé PROFILE prend la valeur par défaut du profil en cours d'utilisation.

Pour les tables de base d'une base de données Microsoft Access, la valeur de la propriété **Connect** est une chaîne nulle ("").

Vous pouvez définir la propriété **Connect** d'un objet **Database** en fournissant un argument source à la méthode **OpenDatabase** . Consultez le paramètre pour connaître le type, le chemin d'accès, l'ID d'utilisateur, le mot de passe ou la source de données ODBC de la base de données.

Dans un objet **QueryDef** d'un espace de travail Microsoft Access, vous pouvez utiliser la propriété **Connect** avec la propriété ReturnsRecords afin de créer une requête SQL directe ODBC. L’argument type_base_données de la chaîne de connexion correspond à "ODBC;" et la chaîne contient ensuite des informations spécifiques du pilote ODBC servant à accéder aux données distantes. Pour plus d'informations, consultez la documentation relative au pilote.


> [!NOTE]
> - Vous devez définir la propriété **Connect** avant de définir la propriété **ReturnsRecords**.
> - Vous devez disposer des autorisations d'accès à l'ordinateur sur lequel se trouve le serveur de base de données auquel vous essayez d'accéder.


