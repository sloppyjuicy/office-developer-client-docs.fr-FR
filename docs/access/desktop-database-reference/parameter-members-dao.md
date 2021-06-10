---
title: Parameter members (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25eae70d88307331c44983c4e7cbbcce3fe9d309
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288111"
---
# <a name="parameter-members-dao"></a><span data-ttu-id="85f44-102">Parameter members (DAO)</span><span class="sxs-lookup"><span data-stu-id="85f44-102">Parameter members (DAO)</span></span>

<span data-ttu-id="85f44-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85f44-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85f44-p101">Un objet Parameter représente une valeur fournie à une requête. Le paramètre est associé à un objet QueryDef créé à partir d'une requête avec paramètres</span><span class="sxs-lookup"><span data-stu-id="85f44-p101">A Parameter object represents a value supplied to a query. The parameter is associated with a QueryDef object created from a parameter query.</span></span>

## <a name="properties"></a><span data-ttu-id="85f44-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="85f44-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85f44-107">Nom</span><span class="sxs-lookup"><span data-stu-id="85f44-107">Name</span></span></p></th>
<th><p><span data-ttu-id="85f44-108">Description</span><span class="sxs-lookup"><span data-stu-id="85f44-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85f44-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span><span class="sxs-lookup"><span data-stu-id="85f44-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85f44-110"><strong>NOTE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="85f44-110"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="85f44-111">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="85f44-111">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="85f44-112">Définit ou renvoit une valeur qui indique si un objet <strong><a href="parameter-object-dao.md">Parameter</a></strong> représente un paramètre d'entrée, de sortie, ou les deux, ou la valeur de retour de la procédure (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="85f44-112">Sets or returns a value that indicates whether a <strong><a href="parameter-object-dao.md">Parameter</a></strong> object represents an input parameter, an output parameter, both, or the return value from the procedure (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85f44-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="85f44-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85f44-p103">Renvoie le nom de l'objet spécifié. En lecture seule <strong>chaîne</strong>.</span><span class="sxs-lookup"><span data-stu-id="85f44-p103">Returns the name of the specified object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85f44-116"><strong><a href="parameter-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="85f44-116"><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85f44-p104">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="85f44-p104">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85f44-119"><strong><a href="parameter-type-property-dao.md">Type</a></strong></span><span class="sxs-lookup"><span data-stu-id="85f44-119"><strong><a href="parameter-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85f44-p105">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type <strong>Integer</strong> en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="85f44-p105">Sets or returns a value that indicates the operational type or data type of an object. Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85f44-122"><strong><a href="parameter-value-property-dao.md">Valeur</a></strong></span><span class="sxs-lookup"><span data-stu-id="85f44-122"><strong><a href="parameter-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85f44-p106">Définit ou renvoie la valeur d'un objet. Type <strong>Variant</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="85f44-p106">Sets or returns the value of an object. Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

