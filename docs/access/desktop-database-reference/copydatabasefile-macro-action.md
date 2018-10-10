---
title: CopierFichierBaseDeDonnées, action de macro
TOCTitle: CopyDatabaseFile Macro Action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b52644cb9a0a5140f45c42eaead84a63723c23e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472054"
---
# <a name="copydatabasefile-macro-action"></a>CopierFichierBaseDeDonnées, action de macro


**S’applique à**: Access 2013 | Office 2013

Utilisez l'action **CopierFichierBaseDeDonnées** pour créer une copie de la base de données Microsoft SQL Server 7.0 (ou version supérieure) active attachée à votre projet Access. Access détache la base de données active, puis l’attache au serveur de destination. Pour plus d'informations sur les procédures permettant de détacher et d'attacher une base de données, voir la documentation de SQL Server.


> [!NOTE]
> <P>[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</P>



## <a name="setting"></a>Valeur

L'action **CopierFichierBaseDeDonnées** possède les arguments suivants.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Nom du fichier de base de données</strong></p></td>
<td><p>Nom du nouveau fichier de données maître. Le chemin d’accès par défaut du fichier est l’emplacement actuel du fichier de projet Access (.adp).</p></td>
</tr>
<tr class="even">
<td><p><strong>Remplacer le fichier existant</strong></p></td>
<td><p>Indique si un fichier existant portant le même nom doit ou non être remplacé. Si cet argument est défini sur <strong>Oui</strong> et si le nom de fichier existe déjà, le fichier est remplacé. S’il est défini sur <strong>Non</strong> et si le nom de fichier existe déjà, le fichier n’est pas remplacé et l’action échoue. Si le fichier n’existe pas déjà, ce paramètre est ignoré. La valeur par défaut est <strong>Oui</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Déconnecter tous les utilisateurs</strong></p></td>
<td><p>Spécifie si Access doit ou non forcer la déconnexion des utilisateurs de la base de données. Si cet argument est défini sur <strong>Oui</strong>, tout utilisateur connecté à la base de données active est déconnecté et l’opération de copie de la base de données peut se poursuivre. S’il est défini sur <strong>Non</strong> et si un ou plusieurs utilisateurs sont connectés à la base de données, l’opération de copie de la base de données échoue. La valeur par défaut est <strong>Non</strong>. 

</p>

> [!WARNING]
> <P>Si les utilisateurs sont déconnectés d’une base de données sans avertissement adéquat, des données risquent d’être perdues.</P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L'opération de copie est une opération synchrone. Vous ne pouvez pas réaliser d'autres opérations jusqu'à ce que la copie de la base de données soit terminée.

L'action **CopierFichierBaseDeDonnées** non seulement copie les données, les définitions de données et les objets de base de données, mais aussi les propriétés étendues, comme les valeurs par défaut, les contraintes de texte et les valeurs de recherche.

Conditions requises pour la copie d'une base de données :

  - vous devez déconnecter toutes les applications et tous les utilisateurs avant de copier le fichier de base de données ;

  - tous les objets et toutes les vues, à l'exception du volet de navigation, doivent être fermés ;

  - la base de données active ne doit pas être répliquée ;

  - la base de données serveur source doit être une base de données Microsoft SQL Server 7.0 ou version supérieure ou une base de données SQL Server 2000 Desktop Engine exécutée sur un ordinateur local ;

<!-- end list -->

  - la base de données SQL Server sur le serveur source doit être un base de données à fichier unique ;

  - vous devez être membre du rôle sysadmin sur les ordinateurs SQL Server source et de destination.

Pour exécuter l'action **CopierFichierBaseDeDonnées** dans un module Visual Basic pour Applications, utilisez la méthode **CopyDatabaseFile** de l'objet **DoCmd**.

