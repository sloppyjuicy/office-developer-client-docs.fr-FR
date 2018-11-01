---
title: Source, propriété (objet Recordset ADO)
TOCTitle: Source Property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32d3d44094e9e5922b7c5e0cfa59ccd1f344ef0f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879136"
---
# <a name="source-property-ado-recordset"></a><span data-ttu-id="5363c-102">Source, propriété (objet Recordset ADO)</span><span class="sxs-lookup"><span data-stu-id="5363c-102">Source Property (ADO Recordset)</span></span>


<span data-ttu-id="5363c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5363c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5363c-104">Indique la source de données d'un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5363c-104">Indicates the data source for a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5363c-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="5363c-105">Settings and return values</span></span>

<span data-ttu-id="5363c-106">Définit une valeur **String** ou une référence à un objet [Command](command-object-ado.md) ; renvoie uniquement une valeur **String** qui indique la source du **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5363c-106">Sets a **String** value or [Command](command-object-ado.md) object reference; returns only a **String** value that indicates the source of the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5363c-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="5363c-107">Remarks</span></span>

<span data-ttu-id="5363c-108">Utilisez la propriété **Source** pour spécifier la source de données d'un objet **Recordset** en utilisant l'une des options suivantes : une variable d'objet **Command**, une instruction SQL, une procédure stockée ou le nom d'une table.</span><span class="sxs-lookup"><span data-stu-id="5363c-108">Use the **Source** property to specify a data source for a **Recordset** object using one of the following: a **Command** object variable, an SQL statement, a stored procedure, or a table name.</span></span>

<span data-ttu-id="5363c-p101">Si vous définissez que la propriété **Source** est un objet **Command**, la propriété [ActiveConnection](activeconnection-property-ado.md) de l'objet **Recordset** hérite sa valeur de la propriété **ActiveConnection** de l'objet **Command** spécifié. Toutefois, la lecture de la propriété **Source** ne renvoie pas un objet **Command**, mais la propriété [CommandText](commandtext-property-ado.md) de l'objet **Command** pour lequel vous avez défini la propriété **Source**.</span><span class="sxs-lookup"><span data-stu-id="5363c-p101">If you set the **Source** property to a **Command** object, the [ActiveConnection](activeconnection-property-ado.md) property of the **Recordset** object will inherit the value of the **ActiveConnection** property for the specified **Command** object. However, reading the **Source** property does not return a **Command** object; instead, it returns the [CommandText](commandtext-property-ado.md) property of the **Command** object to which you set the **Source** property.</span></span>

<span data-ttu-id="5363c-111">Si la propriété **Source** est une instruction SQL, une procédure stockée ou un nom de table, vous pouvez optimiser les performances en passant l’argument *Options* approprié avec l’appel de la méthode [Open](open-method-ado-recordset.md) .</span><span class="sxs-lookup"><span data-stu-id="5363c-111">If the **Source** property is an SQL statement, a stored procedure, or a table name, you can optimize performance by passing the appropriate *Options* argument with the [Open](open-method-ado-recordset.md) method call.</span></span>

<span data-ttu-id="5363c-112">La propriété **Source** est en lecture/écriture pour les objets **Recordset** fermés et lecture seule pour les objets **Recordset** ouverts.</span><span class="sxs-lookup"><span data-stu-id="5363c-112">The **Source** property is read/write for closed **Recordset** objects and read-only for open **Recordset** objects.</span></span>

