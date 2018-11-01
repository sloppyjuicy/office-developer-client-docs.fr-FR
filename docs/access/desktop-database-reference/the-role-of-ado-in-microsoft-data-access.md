---
title: Rôle d'ADO dans Microsoft Data Access
TOCTitle: The Role of ADO in Microsoft Data Access
ms:assetid: e9087ec8-850b-ebbe-369a-a5987a528de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250180(v=office.15)
ms:contentKeyID: 48548433
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 23502ec1bc4ebd0bcdbca17763c2e9dd467d8793
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884519"
---
# <a name="the-role-of-ado-in-microsoft-data-access"></a>Rôle d'ADO dans Microsoft Data Access


**S’applique à**: Access 2013, Office 2013

MDAC (Microsoft Data Access Component) offre un accès aux données indépendant des magasins de données, outils et langages. Ce composant est constitué de deux éléments : une interface conviviale de haut niveau et une interface hautes performances, de bas niveau, permettant d'accéder à pratiquement tous les magasins de données disponibles. Cette souplesse permet d'intégrer des magasins de données divers et d'utiliser votre sélection d'outils, d'applications et de services de plate-forme pour créer des solutions adaptées à vos besoins. Ces technologies constituent la structure sous-jacente de l'accès aux données à usage général dans les systèmes d'exploitation de Microsoft Windows.

MDAC repose sur trois technologies essentielles. ADO, ou ActiveX Data Objects, est une interface conviviale de haut niveau à OLE DB. OLE DB est une interface de bas niveau, hautes performances, permettant d'accéder à un ensemble de magasins de données. ADO et OLE DB peuvent être utilisés conjointement avec des données relationnelles (tabulaires) et non relationnelles (données hiérarchiques ou de flux). Enfin, ODBC, ou Open Database Connectivity, est une autre interface de bas niveau, hautes performances, conçue spécifiquement pour les magasins de données relationnels.

ADO fournit une couche d'abstraction entre votre application cliente ou de niveau intermédiaire et les interfaces OLE DB de bas niveau. ADO utilise un petit groupe d'objets Automation pour fournir à OLE DB une interface simple et efficace. Cette interface fait d'ADO le choix idéal pour les développeurs qui utilisent des langages de niveau supérieur tels que Visual Basic et VBScript, car il permet d'accéder aux données sans devoir maîtriser les subtilités de COM et OLE DB.

