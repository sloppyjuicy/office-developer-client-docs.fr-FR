---
title: Rôle d'ADO dans Microsoft Data Access
TOCTitle: The Role of ADO in Microsoft Data Access
ms:assetid: e9087ec8-850b-ebbe-369a-a5987a528de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250180(v=office.15)
ms:contentKeyID: 48548433
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1675f674a07175b3cade82e5e5b43db29874bec2
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936720"
---
# <a name="the-role-of-ado-in-microsoft-data-access"></a><span data-ttu-id="13c42-102">Rôle d'ADO dans Microsoft Data Access</span><span class="sxs-lookup"><span data-stu-id="13c42-102">The Role of ADO in Microsoft Data Access</span></span>

<span data-ttu-id="13c42-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="13c42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13c42-p101">MDAC (Microsoft Data Access Component) offre un accès aux données indépendant des magasins de données, outils et langages. Ce composant est constitué de deux éléments : une interface conviviale de haut niveau et une interface hautes performances, de bas niveau, permettant d'accéder à pratiquement tous les magasins de données disponibles. Cette souplesse permet d'intégrer des magasins de données divers et d'utiliser votre sélection d'outils, d'applications et de services de plate-forme pour créer des solutions adaptées à vos besoins. Ces technologies constituent la structure sous-jacente de l'accès aux données à usage général dans les systèmes d'exploitation de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="13c42-p101">The Microsoft Data Access Components (MDAC) provide data access that is independent of data stores, tools, and languages. It provides a high-level, easy-to-use interface, and a low-level, high-performance interface to practically any data store available. You can use this flexibility to integrate diverse data stores and use your choice of tools, applications, and platform services to create the right solutions for your needs. These technologies provide the basic framework for general-purpose data access in Microsoft Windows operating systems.</span></span>

<span data-ttu-id="13c42-p102">MDAC repose sur trois technologies essentielles. ADO, ou ActiveX Data Objects, est une interface conviviale de haut niveau à OLE DB. OLE DB est une interface de bas niveau, hautes performances, permettant d'accéder à un ensemble de magasins de données. ADO et OLE DB peuvent être utilisés conjointement avec des données relationnelles (tabulaires) et non relationnelles (données hiérarchiques ou de flux). Enfin, ODBC, ou Open Database Connectivity, est une autre interface de bas niveau, hautes performances, conçue spécifiquement pour les magasins de données relationnels.</span><span class="sxs-lookup"><span data-stu-id="13c42-p102">There are three primary technologies in MDAC. ActiveX Data Objects (ADO) is a high-level, easy-to-use interface to OLE DB. OLE DB is a low-level, high-performance interface to a variety of data stores. ADO and OLE DB both can work with relational (tabular) and nonrelational (hierarchical or stream) data. Finally, Open Database Connectivity (ODBC) is another low-level, high-performance interface that is designed specifically for relational data stores.</span></span>

<span data-ttu-id="13c42-p103">ADO fournit une couche d'abstraction entre votre application cliente ou de niveau intermédiaire et les interfaces OLE DB de bas niveau. ADO utilise un petit groupe d'objets Automation pour fournir à OLE DB une interface simple et efficace. Cette interface fait d'ADO le choix idéal pour les développeurs qui utilisent des langages de niveau supérieur tels que Visual Basic et VBScript, car il permet d'accéder aux données sans devoir maîtriser les subtilités de COM et OLE DB.</span><span class="sxs-lookup"><span data-stu-id="13c42-p103">ADO provides a layer of abstraction between your client or middle-tier application and the low-level OLE DB interfaces. ADO uses a small set of Automation objects to provide a simple and efficient interface to OLE DB. This interface makes ADO the perfect choice for developers in higher level languages, such as Visual Basic and even VBScript, who want to access data without having to learn the intricacies of COM and OLE DB.</span></span>

