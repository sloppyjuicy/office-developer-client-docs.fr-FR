---
title: Using the Connection Object (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd3e691258fe5950f40c36a1efcaed8e79810c7a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470284"
---
# <a name="using-the-connection-object-access"></a>Using the Connection Object (Access)


**S’applique à**: Access 2013 | Office 2013

Un objet **Connection** représente une session unique associée à une source de données. Dans le cas d'un système de base de données client/serveur, il peut être apparenté à une connexion réseau au serveur. Selon les fonctionnalités prises en charge par le fournisseur, il est possible que certaines collections, méthodes ou propriétés d'un objet **Connection** ne soient pas disponibles.

Avant d'ouvrir un objet **Connection**, vous devez définir certaines informations concernant la source de données et le type de connexion. Le paramètre *ConnectionString* de la méthode **Open** de l’objet **Connection** , ou la propriété **ConnectionString** de l’objet **Connection** , contient généralement la plupart de ces informations. Une chaîne de connexion est une chaîne de caractères qui définit un nombre variable d'arguments. Les arguments , qu'ils soient requis par ADO ou spécifiques au fournisseur, contiennent les informations dont l'objet **Connection** a besoin pour établir la connexion. Les arguments constituant le paramètre *ConnectionString* sont séparés par des points-virgules ( ;).


> [!NOTE]
> <P>Vous pouvez également spécifier un fichier DSN (Data Source Name) ODBC ou UDL (Data Link) dans une chaîne de connexion. Pour plus d'informations sur les fichiers DSN, consultez la section Data Sources dans la première partie du manuel <EM>ODBC Programmer's Reference</EM> (en anglais). Pour plus d'informations sur les fichiers UDL, consultez la section Data Link API Overview du manuel <EM>OLE DB Programmer's Reference</EM> (en anglais).</P>


