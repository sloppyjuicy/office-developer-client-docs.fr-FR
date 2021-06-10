---
title: Document.LastUpdated, propriété (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abb766f7a47cbacaededf65eb2b5e9145bf88c60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293804"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="4b20f-102">Document.LastUpdated, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="4b20f-102">Document.LastUpdated property (DAO)</span></span>


<span data-ttu-id="4b20f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b20f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b20f-p101">Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données **Variant** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4b20f-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b20f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b20f-106">Syntax</span></span>

<span data-ttu-id="4b20f-107">*.* LastUpdated</span><span class="sxs-lookup"><span data-stu-id="4b20f-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="4b20f-108">*expression* Variable qui représente un **objet Document.**</span><span class="sxs-lookup"><span data-stu-id="4b20f-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b20f-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="4b20f-109">Remarks</span></span>

<span data-ttu-id="4b20f-p102">**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="4b20f-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

