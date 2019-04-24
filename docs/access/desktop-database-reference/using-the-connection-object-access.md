---
title: Using the Connection Object (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d16b802140e2dcbbd85988bee316ae27236c3235
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305921"
---
# <a name="using-the-connection-object-access"></a>Utilisation de l'objet Connection (Access)


**S’applique à** : Access 2013, Office 2013

Un objet **Connection** représente une session unique associée à une source de données. Dans le cas d'un système de base de données client/serveur, il peut être apparenté à une connexion réseau au serveur. Selon les fonctionnalités prises en charge par le fournisseur, il est possible que certaines collections, méthodes ou propriétés d'un objet **Connection** ne soient pas disponibles.

Avant d'ouvrir un objet **Connection**, vous devez définir certaines informations concernant la source de données et le type de connexion. Le paramètre *ConnectionString* de la méthode **Open** de l'objet **Connection**, ou la propriété **ConnectionString** de l'objet **Connection** , contient généralement la plupart de ces informations. Une chaîne de connexion est une chaîne de caractères qui définit un nombre variable d'arguments. Les arguments , qu'ils soient requis par ADO ou spécifiques au fournisseur, contiennent les informations dont l'objet **Connection** a besoin pour établir la connexion. Les arguments constituant le paramètre *ConnectionString* sont séparés par des points-virgules (;).

> [!NOTE]
> Vous pouvez également spécifier un fichier DSN (Data Source Name) ODBC ou UDL (Data Link) dans une chaîne de connexion. Pour plus d'informations sur les fichiers DSN, consultez la section Data Sources dans la première partie du manuel *ODBC Programmer's Reference* (en anglais). Pour plus d'informations sur les fichiers UDL, consultez la section Data Link API Overview du manuel *OLE DB Programmer's Reference* (en anglais).

Cette section contient les rubriques suivantes :

- [Création de la chaîne de connexion](creating-the-connection-string.md)
- [Contrôle des transactions](controlling-transactions.md)
