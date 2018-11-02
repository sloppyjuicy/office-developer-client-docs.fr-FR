---
title: Propriété TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b24aaa5aec9b17adc169c67733a19a9077a4930
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920920"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="0f93d-102">Propriété TableDef.RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="0f93d-102">TableDef.RecordCount property (DAO)</span></span>


<span data-ttu-id="0f93d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f93d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0f93d-p101">Renvoie le nombre total d'enregistrements dans un objet **[TableDef](tabledef-object-dao.md)**. Type de données **Long** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0f93d-p101">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f93d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f93d-106">Syntax</span></span>

<span data-ttu-id="0f93d-107">*expression* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="0f93d-107">*expression* .RecordCount</span></span>

<span data-ttu-id="0f93d-108">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="0f93d-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f93d-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="0f93d-109">Remarks</span></span>

<span data-ttu-id="0f93d-110">Un objet **Recordset** ou **TableDef** sans enregistrements a une valeur de propriété **RecordCount** égale à 0.</span><span class="sxs-lookup"><span data-stu-id="0f93d-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="0f93d-111">Lorsque vous travaillez avec des objets **TableDef** liés, la valeur de la propriété **RecordCount** est toujours égale à –1.</span><span class="sxs-lookup"><span data-stu-id="0f93d-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

