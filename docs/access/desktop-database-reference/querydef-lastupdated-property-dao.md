---
title: Propriété QueryDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98bb600e6f3f1c9587eca110269e8b6b3765e40f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921270"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="bafaf-102">Propriété QueryDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="bafaf-102">QueryDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="bafaf-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bafaf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bafaf-p101">Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données **Variant** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="bafaf-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bafaf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bafaf-106">Syntax</span></span>

<span data-ttu-id="bafaf-107">*expression* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="bafaf-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="bafaf-108">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="bafaf-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bafaf-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="bafaf-109">Remarks</span></span>

<span data-ttu-id="bafaf-p102">**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="bafaf-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

