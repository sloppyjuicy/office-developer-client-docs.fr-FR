---
title: CancelUpdate, méthode (RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0c02a9ca72add763e1d3ccf62d5ede8adaecc6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296667"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="4b8f9-102">CancelUpdate, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="4b8f9-102">CancelUpdate method (RDS)</span></span>

<span data-ttu-id="4b8f9-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b8f9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b8f9-104">Annule toutes les modifications apportées à la ligne active ou à une nouvelle ligne d’un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4b8f9-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b8f9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b8f9-105">Syntax</span></span>

<span data-ttu-id="4b8f9-106">*DataControl*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="4b8f9-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="4b8f9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b8f9-107">Parameters</span></span>

|<span data-ttu-id="4b8f9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b8f9-108">Parameter</span></span>|<span data-ttu-id="4b8f9-109">Description</span><span class="sxs-lookup"><span data-stu-id="4b8f9-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4b8f9-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="4b8f9-110">*DataControl*</span></span> |<span data-ttu-id="4b8f9-111">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="4b8f9-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4b8f9-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="4b8f9-112">Remarks</span></span>

<span data-ttu-id="4b8f9-p101">Le service de curseur pour OLE DB conserve à la fois une copie des valeurs d'origine et un cache des modifications. Lorsque vous appelez la méthode **CancelUpdate**, le cache des modifications est réinitialisé et vidé et tous les contrôles dépendants sont actualisés avec les données d'origine.</span><span class="sxs-lookup"><span data-stu-id="4b8f9-p101">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes. When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

