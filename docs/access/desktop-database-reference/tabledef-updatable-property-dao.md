---
title: Propriété TableDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 71202203588182ba2bf1ba1449f2b1ee04c82c67
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926198"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="7980b-102">Propriété TableDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="7980b-102">TableDef.Updatable property (DAO)</span></span>


<span data-ttu-id="7980b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7980b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7980b-p101">Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type **Boolean** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7980b-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7980b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7980b-106">Syntax</span></span>

<span data-ttu-id="7980b-107">*expression* . Mise à jour</span><span class="sxs-lookup"><span data-stu-id="7980b-107">*expression* .Updatable</span></span>

<span data-ttu-id="7980b-108">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="7980b-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7980b-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="7980b-109">Remarks</span></span>

<span data-ttu-id="7980b-p102">La valeur de la propriété **Updatable** est toujours **True** pour un nouvel objet **TableDef** nouvellement créé et **False** pour un objet **TableDef** lié. Un nouvel objet **TableDef** peut être ajouté uniquement à une base de données pour laquelle l'utilisateur actif possède une autorisation en écriture.</span><span class="sxs-lookup"><span data-stu-id="7980b-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>

