---
title: TableDef.Updatable, propriété (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6e6c7409b89058c6be55d9fb83eb85c7af9fb9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314412"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="de318-102">TableDef.Updatable, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="de318-102">TableDef.Updatable property (DAO)</span></span>


<span data-ttu-id="de318-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="de318-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de318-p101">Renvoie une valeur qui indique si vous pouvez changer un objet DAO. Type de données **Boolean** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="de318-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="de318-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de318-106">Syntax</span></span>

<span data-ttu-id="de318-107">*.* Updatable</span><span class="sxs-lookup"><span data-stu-id="de318-107">*expression* .Updatable</span></span>

<span data-ttu-id="de318-108">*expression* Variable représentant un objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="de318-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="de318-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="de318-109">Remarks</span></span>

<span data-ttu-id="de318-p102">La valeur de la propriété **Updatable** est toujours **True** pour un nouvel objet **TableDef** nouvellement créé et **False** pour un objet **TableDef** lié. Un nouvel objet **TableDef** peut être ajouté uniquement à une base de données pour laquelle l'utilisateur actif possède une autorisation en écriture.</span><span class="sxs-lookup"><span data-stu-id="de318-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>

