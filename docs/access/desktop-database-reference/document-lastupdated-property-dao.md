---
title: Propriété Document.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 57fb558330c602206831c1c72f09a13094eba799
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927311"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="9a320-102">Propriété Document.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="9a320-102">Document.LastUpdated property (DAO)</span></span>


<span data-ttu-id="9a320-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a320-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a320-p101">Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données **Variant** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9a320-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a320-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a320-106">Syntax</span></span>

<span data-ttu-id="9a320-107">*expression* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="9a320-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="9a320-108">*expression* Variable qui représente un objet **Document** .</span><span class="sxs-lookup"><span data-stu-id="9a320-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a320-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="9a320-109">Remarks</span></span>

<span data-ttu-id="9a320-p102">**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="9a320-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

