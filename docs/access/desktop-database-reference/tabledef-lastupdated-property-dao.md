---
title: Propriété TableDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 81d8dfd040ef7df954b71f724ed1d2689d5d4b33
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928221"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="7bd6e-102">Propriété TableDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="7bd6e-102">TableDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="7bd6e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7bd6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7bd6e-p101">Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données **Variant** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bd6e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bd6e-106">Syntax</span></span>

<span data-ttu-id="7bd6e-107">*expression* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="7bd6e-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="7bd6e-108">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="7bd6e-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bd6e-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="7bd6e-109">Remarks</span></span>

<span data-ttu-id="7bd6e-p102">**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

