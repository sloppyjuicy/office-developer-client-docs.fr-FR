---
title: TableDef.DateCreated, propriété (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5dc326b271e8444211bba0cd2d3c37c047ac205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314538"
---
# <a name="tabledefdatecreated-property-dao"></a><span data-ttu-id="55119-102">TableDef.DateCreated, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="55119-102">TableDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="55119-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="55119-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="55119-p101">Renvoie la date et l'heure auxquelles un objet a été créé (espaces de travail Microsoft Access uniquement). Valeur **Variant** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="55119-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="55119-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55119-106">Syntax</span></span>

<span data-ttu-id="55119-107">*.* DateCreated</span><span class="sxs-lookup"><span data-stu-id="55119-107">*expression* .DateCreated</span></span>

<span data-ttu-id="55119-108">*expression* Variable représentant un objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="55119-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="55119-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="55119-109">Remarks</span></span>

<span data-ttu-id="55119-p102">**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="55119-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

