---
title: QueryDef. LastUpdated, propriété (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1876e92381828075edca3bbfcbae63e706a21365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303310"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="2158a-102">QueryDef. LastUpdated, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="2158a-102">QueryDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="2158a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2158a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2158a-104">Renvoie la date et l'heure de la dernière modification apportée à un objet.</span><span class="sxs-lookup"><span data-stu-id="2158a-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="2158a-105">Type de données **Variant** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2158a-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2158a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2158a-106">Syntax</span></span>

<span data-ttu-id="2158a-107">*expression* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="2158a-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="2158a-108">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="2158a-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2158a-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="2158a-109">Remarks</span></span>

<span data-ttu-id="2158a-p102">**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="2158a-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

