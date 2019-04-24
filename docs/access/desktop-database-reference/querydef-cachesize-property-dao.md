---
title: QueryDef. CacheSize, propriété (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d826781bd668cff0a61c655e55834512a289c17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301091"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="8ee97-102">QueryDef. CacheSize, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="8ee97-102">QueryDef.CacheSize property (DAO)</span></span>


<span data-ttu-id="8ee97-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ee97-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ee97-104">Définit ou renvoie le nombre d'enregistrements extraits d'une source de données ODBC qui seront placés dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="8ee97-104">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="8ee97-105">Type de données **Long** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="8ee97-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ee97-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ee97-106">Syntax</span></span>

<span data-ttu-id="8ee97-107">*expression* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="8ee97-107">*expression* .CacheSize</span></span>

<span data-ttu-id="8ee97-108">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="8ee97-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ee97-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="8ee97-109">Remarks</span></span>

<span data-ttu-id="8ee97-p102">La valeur de la propriété **CacheSize** doit être comprise entre 5 et 1 200, tout en ne dépassant pas la mémoire disponible. La valeur habituelle est égale à 100. La valeur 0 désactive la mise en cache.</span><span class="sxs-lookup"><span data-stu-id="8ee97-p102">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.</span></span>

<span data-ttu-id="8ee97-113">Le moteur de base de données Microsoft Access demande au cache les enregistrements dans la plage du cache et extrait les enregistrements situés en dehors de cette plage à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="8ee97-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="8ee97-114">Les enregistrements extraits du cache ne répercutent pas les modifications simultanées apportées aux données sources par les autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8ee97-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

