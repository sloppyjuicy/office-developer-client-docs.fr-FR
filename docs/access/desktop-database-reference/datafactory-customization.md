---
title: Personnalisation DataFactory
TOCTitle: DataFactory customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b69ed36acb84e12927d69fcb7b4df102a792f5d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585871"
---
# <a name="datafactory-customization"></a>Personnalisation DataFactory


**S’applique à** : Access 2013, Office 2013

RDS (Remote Data Service) permet d'accéder facilement aux données dans un système client/serveur à trois niveaux. Un contrôle des données client spécifie des paramètres de chaîne de connexion et de commande pour exécuter une requête sur une source de données distante ou des paramètres de chaîne de connexion et d'objet [Recordset](recordset-object-ado.md) pour effectuer des mises à jour.

Les paramètres sont transmis à un programme serveur qui effectue l'opération d'accès aux données sur la source de données distante. RDS fournit un programme serveur par défaut, l'objet [RDSServer.DataFactory](datafactory-object-rdsserver.md). L'objet **RDSServer.DataFactory** retourne tout objet **Recordset** résultant d'une requête au client.

Toutefois, l'objet **RDSServer.DataFactory** ne peut effectuer que des requêtes et des mises à jour. Il ne peut pas effectuer d'opérations de validation ni de traitement sur les chaînes de connexion ou de commande.

Avec ADO, vous pouvez spécifier que **DataFactory** doit fonctionner en association avec un autre type de programme serveur appelé *gestionnaire*. Le gestionnaire peut modifier les chaînes de commande et de connexion cliente avant qu'elles soient utilisées pour accéder à la source de données. En outre, le gestionnaire peut appliquer des droits d'accès qui permettent au client de lire et d'écrire des données dans la source de données.

Les paramètres utilisés par le gestionnaire pour modifier les paramètres et les droits d'accès du client sont spécifiés dans les sections d'un fichier de personnalisation.

Consultez les rubriques suivantes pour plus d'informations sur la personnalisation de l'objet **DataFactory**:

- [Présentation du fichier de personnalisation](understanding-the-customization-file.md)
- [Section de connexion du fichier de personnalisation](customization-file-connect-section.md)
- [Section SQL du fichier de personnalisation](customization-file-sql-section.md)
- [Section UserList du fichier de personnalisation](customization-file-userlist-section.md)
- [Section des journaux du fichier de personnalisation](customization-file-logs-section.md)
- [Paramètres clients obligatoires](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)
- [Écriture de votre propre handler personnalisé](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
