---
title: Résumé du modèle objet RDS
TOCTitle: RDS object model summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33cbdc6de644592d87b7d49e65a5c5674ad94d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300874"
---
# <a name="rds-object-model-summary"></a><span data-ttu-id="a9979-102">Résumé du modèle objet RDS</span><span class="sxs-lookup"><span data-stu-id="a9979-102">RDS object model summary</span></span>


<span data-ttu-id="a9979-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9979-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9979-104">Objet</span><span class="sxs-lookup"><span data-stu-id="a9979-104">Object</span></span></p></th>
<th><p><span data-ttu-id="a9979-105">Description</span><span class="sxs-lookup"><span data-stu-id="a9979-105">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9979-106"><a href="dataspace-object-rds.md">RDS. DataSpace</a></span><span class="sxs-lookup"><span data-stu-id="a9979-106"><a href="dataspace-object-rds.md">RDS.DataSpace</a></span></span></p></td>
<td><p><span data-ttu-id="a9979-p101">Cet objet contient une méthode permettant d’obtenir un proxy serveur qui peut être le proxy par défaut ou un programme serveur personnalisé (objet métier). Le programme serveur peut être appelé sur Internet, un intranet, un réseau local ou être une bibliothèque de liens dynamiques locale.</span><span class="sxs-lookup"><span data-stu-id="a9979-p101">This object contains a method to obtain a server proxy. The proxy may be the default or a custom server program (business object). The server program may be invoked on the Internet, an intranet, a local area network, or be a local dynamic-link library.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9979-110"><a href="datafactory-object-rdsserver.md">RDSServer. DataFactory</a></span><span class="sxs-lookup"><span data-stu-id="a9979-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span></span></p></td>
<td><p><span data-ttu-id="a9979-111">Cet objet représente le programme serveur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a9979-111">This object represents the default server program.</span></span> <span data-ttu-id="a9979-112">Il met en œuvre le comportement par défaut d'extraction et de mise à jour des données RDS.</span><span class="sxs-lookup"><span data-stu-id="a9979-112">It executes the default RDS data retrieval and update behavior.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9979-113"><a href="datacontrol-object-rds.md">RDS. RDS</a></span><span class="sxs-lookup"><span data-stu-id="a9979-113"><a href="datacontrol-object-rds.md">RDS.DataControl</a></span></span></p></td>
<td><p><span data-ttu-id="a9979-114">Cet objet est capable d'appeler automatiquement les objets <strong>RDS.DataSpace</strong> et <strong>RDSServer.DataFactory</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9979-114">This object can automatically invoke the <strong>RDS.DataSpace</strong> and <strong>RDSServer.DataFactory</strong> objects.</span></span> <span data-ttu-id="a9979-115">Utilisez-le pour appeler le comportement par défaut d'extraction ou de mise à jour des données RDS.</span><span class="sxs-lookup"><span data-stu-id="a9979-115">Use this object to invoke the default RDS data retrieval or update behavior.</span></span> <span data-ttu-id="a9979-116">Cet objet permet également aux contrôles visuels d'accéder à l'objet <strong>Recordset</strong> retourné.</span><span class="sxs-lookup"><span data-stu-id="a9979-116">This object also provides the means for visual controls to access the returned <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

