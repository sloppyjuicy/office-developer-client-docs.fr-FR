---
title: TableDef.RecordCount Property (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b1d1ab4fee16a9664733c71522cb07a49dde149
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470879"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="7babe-102">TableDef.RecordCount Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="7babe-102">TableDef.RecordCount Property (DAO)</span></span>


<span data-ttu-id="7babe-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7babe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7babe-p101">Renvoie le nombre total d'enregistrements dans un objet **[TableDef](tabledef-object-dao.md)**. Type de données **Long** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7babe-p101">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7babe-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7babe-106">Syntax</span></span>

<span data-ttu-id="7babe-107">*expression* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="7babe-107">*expression* .RecordCount</span></span>

<span data-ttu-id="7babe-108">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="7babe-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7babe-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="7babe-109">Remarks</span></span>

<span data-ttu-id="7babe-110">Un objet **Recordset** ou **TableDef** sans enregistrements a une valeur de propriété **RecordCount** égale à 0.</span><span class="sxs-lookup"><span data-stu-id="7babe-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="7babe-111">Lorsque vous travaillez avec des objets **TableDef** liés, la valeur de la propriété **RecordCount** est toujours égale à –1.</span><span class="sxs-lookup"><span data-stu-id="7babe-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

