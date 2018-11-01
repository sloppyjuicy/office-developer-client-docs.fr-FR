---
title: Document.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad5a84dcc1765cc90fdfb08adfb6610be7057401
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879647"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="beef1-102">Document.LastUpdated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="beef1-102">Document.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="beef1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="beef1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="beef1-p101">Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données **Variant** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="beef1-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="beef1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="beef1-106">Syntax</span></span>

<span data-ttu-id="beef1-107">*expression* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="beef1-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="beef1-108">*expression* Variable qui représente un objet **Document** .</span><span class="sxs-lookup"><span data-stu-id="beef1-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="beef1-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="beef1-109">Remarks</span></span>

<span data-ttu-id="beef1-p102">**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="beef1-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

