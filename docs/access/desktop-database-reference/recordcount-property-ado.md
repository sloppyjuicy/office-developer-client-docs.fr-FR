---
title: RecordCount, propriété (ADO)
TOCTitle: RecordCount property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d5ab01c419f703c1c17b1bf2b2cca2fb3844655d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300769"
---
# <a name="recordcount-property-ado"></a><span data-ttu-id="1d040-102">RecordCount, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="1d040-102">RecordCount property (ADO)</span></span>


<span data-ttu-id="1d040-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d040-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d040-104">Indique le nombre d’enregistrements dans un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1d040-104">Indicates the number of records in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d040-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1d040-105">Return value</span></span>

<span data-ttu-id="1d040-106">Retourne une valeur de type **Long** qui indique le nombre d'enregistrements dans le **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1d040-106">Returns a **Long** value that indicates the number of records in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d040-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="1d040-107">Remarks</span></span>

<span data-ttu-id="1d040-p101">Utilisez la propriété **RecordCount** pour connaître le nombre d'enregistrements dans un objet **Recordset**. La propriété renvoie -1 quand ADO ne parvient pas à déterminer le nombre d'enregistrements ou si le fournisseur (ou le type de cursor) ne prend pas en charge la propriété **RecordCount**. Les tentatives de lecture de la propriété **RecordCount** sur un **Recordset** fermé génèrent une erreur.</span><span class="sxs-lookup"><span data-stu-id="1d040-p101">Use the **RecordCount** property to find out how many records are in a **Recordset** object. The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**. Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="1d040-p102">Si l'objet **Recordset** prend en charge le positionnement approximatif ou les signets (c'est-à-dire si **Supports (adApproxPosition)** ou **Supports (adBookmark)**, respectivement, renvoient la valeur **True** ) cette valeur est égale au nombre exact d'enregistrements dans le **Recordset**, qu'il soit complet ou non. Si l'objet **Recordset** ne prend pas en charge le positionnement approximatif, il se peut que cette propriété représente une charge significative pour les ressources, car tous les enregistrements devront être récupérés et comptés pour qu'une valeur **RecordCount** précise puisse être renvoyée.</span><span class="sxs-lookup"><span data-stu-id="1d040-p102">If the **Recordset** object supports approximate positioning or bookmarks — that is, **Supports (adApproxPosition)** or **Supports (adBookmark)**, respectively, return **True** — this value will be the exact number of records in the **Recordset**, regardless of whether it has been fully populated. If the **Recordset** object does not support approximate positioning, this property may be a significant drain on resources because all records will have to be retrieved and counted to return an accurate **RecordCount** value.</span></span>

<span data-ttu-id="1d040-p103">Le type de curseur de l'objet **Recordset** détermine si les enregistrements pourront ou ne pourront pas être comptés. La propriété **RecordCount** renvoie -1 si le curseur est de type avant uniquement. Elle renvoie le nombre réel d'enregistrements si le curseur est statique ou basé sur un jeu de clé et -1 ou soit le nombre d'enregistrements si le curseur est dynamique (cela dépend alors de la source de données).</span><span class="sxs-lookup"><span data-stu-id="1d040-p103">The cursor type of the **Recordset** object affects whether the number of records can be determined. The **RecordCount** property will return -1 for a forward-only cursor; the actual count for a static or keyset cursor; and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

