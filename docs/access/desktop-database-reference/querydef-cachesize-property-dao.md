---
title: QueryDef.CacheSize Property (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1ecddf9a9972c6ded5e28748822169c2c60edc44
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469259"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="1afef-102">QueryDef.CacheSize Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="1afef-102">QueryDef.CacheSize Property (DAO)</span></span>


<span data-ttu-id="1afef-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1afef-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1afef-p101">Définit ou renvoie le nombre d'enregistrements extraits d'une source de données ODBC qui seront placés dans le cache local. Valeur **Long** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="1afef-p101">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1afef-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1afef-106">Syntax</span></span>

<span data-ttu-id="1afef-107">*expression* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="1afef-107">*expression* .CacheSize</span></span>

<span data-ttu-id="1afef-108">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="1afef-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1afef-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="1afef-109">Remarks</span></span>

<span data-ttu-id="1afef-p102">La valeur de la propriété **CacheSize** doit être comprise entre 5 et 1 200, tout en ne dépassant pas la mémoire disponible. La valeur habituelle est égale à 100. La valeur 0 désactive la mise en cache.</span><span class="sxs-lookup"><span data-stu-id="1afef-p102">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.</span></span>

<span data-ttu-id="1afef-113">Le moteur de base de données Microsoft Access demande au cache les enregistrements dans la plage du cache et extrait les enregistrements situés en dehors de cette plage à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="1afef-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="1afef-114">Les enregistrements extraits du cache ne répercutent pas les modifications simultanées apportées aux données sources par les autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1afef-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

