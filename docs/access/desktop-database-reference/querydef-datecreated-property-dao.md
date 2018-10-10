---
title: QueryDef.DateCreated Property (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62fcad68a50ac7f2a09675d9ac51734c4147d207
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472037"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="ad29c-102">QueryDef.DateCreated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="ad29c-102">QueryDef.DateCreated Property (DAO)</span></span>


<span data-ttu-id="ad29c-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad29c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ad29c-p101">Renvoie la date et l'heure auxquelles un objet a été créé (espaces de travail Microsoft Access uniquement). Valeur **Variant** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ad29c-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad29c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad29c-106">Syntax</span></span>

<span data-ttu-id="ad29c-107">*expression* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="ad29c-107">*expression* .DateCreated</span></span>

<span data-ttu-id="ad29c-108">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="ad29c-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad29c-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="ad29c-109">Remarks</span></span>

<span data-ttu-id="ad29c-p102">**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="ad29c-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

