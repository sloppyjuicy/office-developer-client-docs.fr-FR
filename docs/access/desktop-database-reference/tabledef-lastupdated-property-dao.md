---
title: TableDef.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3840ef8b2a01f28bd2a9881848c813f85411fb7b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471154"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="a1f71-102">TableDef.LastUpdated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="a1f71-102">TableDef.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="a1f71-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1f71-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a1f71-p101">Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données **Variant** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a1f71-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f71-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1f71-106">Syntax</span></span>

<span data-ttu-id="a1f71-107">*expression* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="a1f71-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="a1f71-108">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="a1f71-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1f71-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="a1f71-109">Remarks</span></span>

<span data-ttu-id="a1f71-p102">**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="a1f71-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

