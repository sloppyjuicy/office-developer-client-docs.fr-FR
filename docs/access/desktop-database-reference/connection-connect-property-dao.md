---
title: Connection.Connect Property (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a362f2d480a27341620695038e6507083ae5ed81
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861840"
---
# <a name="connectionconnect-property-dao"></a>Connection.Connect Property (DAO)


**S’applique à**: Access 2013 | Office 2013

Définit ou renvoie une valeur qui fournit des informations sur la source d'une connexion ouverte. Valeur de type **String** en lecture/écriture.

## <a name="syntax"></a>Syntaxe

*expression* . Se connecter

*expression* Variable qui représente un objet **Connection** .

## <a name="remarks"></a>Remarques

Le paramètre de la propriété **Connect** est une valeur **String** constituée d'un spécificateur de type de base de données et de paramètres séparés par des points-virgules (ou aucun paramètre). La propriété **Connect** transmet des informations supplémentaires à ODBC et à certains pilotes ISAM, si nécessaire.

Pour exécuter une requête SQL directe sur une table liée au fichier de base de données Microsoft Access, vous devez d'abord définir la propriété **Connect** de la base de données de la table liée sur une chaîne de connexion ODBC valide.

Dans le cas d'un objet **TableDef** représentant une table liée, la valeur de la propriété **Connect** est constituée d'un ou de deux éléments (un spécificateur de type de base de données et un chemin d'accès à la base de données), se terminant chacun par un point-virgule.

Le chemin d'accès indiqué dans le tableau ci-dessous correspond au chemin d'accès complet au répertoire contenant les fichiers de base de données. Il doit être précédé de l'identificateur DATABASE=. Dans certains cas (bases de données du moteur de base de données Microsoft Access et Microsoft Excel, par exemple), vous devez inclure un nom de fichier spécifique dans l'argument du chemin d'accès à la base de données.

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
<td><p>[base de données ;]</p></td>
<td><p>lecteur:\chemin_accès\nom_fichier</p></td>
</tr>
<tr class="even">
<td><p>dBASE III</p></td>
<td><p>dBASE III;</p></td>
<td><p>lecteur : \path</p></td>
</tr>
<tr class="odd">
<td><p>dBASE IV</p></td>
<td><p>dBASE IV;</p></td>
<td><p>lecteur : \path</p></td>
</tr>
<tr class="even">
<td><p>dBASE 5</p></td>
<td><p>dBASE 5.0;</p></td>
<td><p>lecteur : \path</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 3.x</p></td>
<td><p>Paradox 3.x;</p></td>
<td><p>lecteur : \path</p></td>
</tr>
<tr class="even">
<td><p>Paradox 4.x</p></td>
<td><p>Paradox 4.x;</p></td>
<td><p>lecteur : \path</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 5.x</p></td>
<td><p>Paradox 5.x;</p></td>
<td><p>lecteur : \path</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 3.0</p></td>
<td><p>Excel 3.0;</p></td>
<td><p>Drive:\path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 4.0</p></td>
<td><p>Excel 4.0;</p></td>
<td><p>Drive:\path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 5.0 or Microsoft Excel 95</p></td>
<td><p>Excel 5.0;</p></td>
<td><p>Drive:\path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 97</p></td>
<td><p>Excel 8.0;</p></td>
<td><p>Drive:\path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WKS et WK1</p></td>
<td><p>Lotus WK1;</p></td>
<td><p>Drive:\path\filename.wk1</p></td>
</tr>
<tr class="odd">
<td><p>Lotus 1-2-3 WK3</p></td>
<td><p>Lotus WK3;</p></td>
<td><p>Drive:\path\filename.wk3</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WK4</p></td>
<td><p>Lotus WK4;</p></td>
<td><p>Drive:\path\filename.wk4</p></td>
</tr>
<tr class="odd">
<td><p>Importation HTML</p></td>
<td><p>HTML Import;</p></td>
<td><p>lecteur:\chemin_accès\nom_fichier</p></td>
</tr>
<tr class="even">
<td><p>Exportation HTML</p></td>
<td><p>HTML Export;</p></td>
<td><p>lecteur : \path</p></td>
</tr>
<tr class="odd">
<td><p>Texte</p></td>
<td><p>Text;</p></td>
<td><p>lecteur : \path</p></td>
</tr>
<tr class="even">
<td><p>ODBC</p></td>
<td><p>ODBC ; Base de données = base de données ; UID = utilisateur ; PWD = mot de passe ; DSN = NomSourceDonnées ; [LOGINTIMEOUT = secondes ;]</p></td>
<td><p>Aucune</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Exchange</p></td>
<td><p>Exchange 4.0 ; MAPILEVEL = CheminDossier ; [TABLETYPE = {0 | 1}] ; [PROFILE = profil ;] [PWD = mot de passe ;] [Base de données = base de données ;]</p></td>
<td><p>lecteur:\chemin_accès\nom_fichier</p></td>
</tr>
</tbody>
</table>


Si le spécificateur est uniquement "ODBC;", le pilote ODBC affiche une boîte de dialogue répertoriant tous les noms des sources de données ODBC enregistrées pour permettre à l'utilisateur de sélectionner une base de données.

Si un mot de passe est obligatoire et qu'il n'est pas fourni par la propriété **Connect**, une boîte de dialogue de connexion s'affiche la première fois que le pilote ODBC accède à une table et une nouvelle fois si la connexion est fermée et rouverte.

Pour les données dans Microsoft Exchange, la clé MAPILEVEL obligatoire doit être définie avec un chemin de dossier entièrement résolu (par exemple, « Mailbox - Pat SmithIAlpha/Today »). Le chemin d’accès n’inclut pas le nom du dossier qui s’ouvre sous forme de tableau ; nom du dossier doit être spécifié à la place l’argument nom de la méthode **Create table** . La clé TABLETYPE doit avoir la valeur « 0 » pour ouvrir un dossier (par défaut) ou « 1 » pour ouvrir un carnet d'adresses. La clé PROFILE prend la valeur par défaut du profil en cours d'utilisation.

Pour les tables de base d'une base de données Microsoft Access, la valeur de la propriété **Connect** est une chaîne nulle ("").

Vous pouvez définir la propriété **Connect** d’un objet de **base de données** en fournissant un argument source dans la méthode **OpenDatabase** . Consultez le paramètre pour connaître le type, le chemin d'accès, l'ID d'utilisateur, le mot de passe ou la source de données ODBC de la base de données.

Dans un objet **QueryDef** d'un espace de travail Microsoft Access, vous pouvez utiliser la propriété **Connect** avec la propriété ReturnsRecords afin de créer une requête SQL directe ODBC. Databasetype de la chaîne de connexion est « ODBC ; », et le reste de la chaîne contient des informations spécifiques au pilote ODBC utilisé pour accéder aux données à distance. Pour plus d'informations, consultez la documentation relative au pilote.


> [!NOTE]
> - Vous devez définir la propriété **Connect** avant de définir la propriété **ReturnsRecords**.
> - Vous devez disposer des autorisations d'accès à l'ordinateur sur lequel se trouve le serveur de base de données auquel vous essayez d'accéder.


