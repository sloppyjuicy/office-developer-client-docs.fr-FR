---
title: QueryDef. DateCreated, propriété (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4a120eed6c20db73e1c23f31ea9329d00da2f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301070"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="cc6cd-102">QueryDef. DateCreated, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="cc6cd-102">QueryDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="cc6cd-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc6cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc6cd-104">Renvoie la date et l'heure auxquelles un objet a été créé (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="cc6cd-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="cc6cd-105">Type **Variant** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc6cd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc6cd-106">Syntax</span></span>

<span data-ttu-id="cc6cd-107">*expression* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="cc6cd-107">*expression* .DateCreated</span></span>

<span data-ttu-id="cc6cd-108">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="cc6cd-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc6cd-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="cc6cd-109">Remarks</span></span>

<span data-ttu-id="cc6cd-p102">**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

