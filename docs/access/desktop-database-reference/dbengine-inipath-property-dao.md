---
title: Propriété DBEngine.IniPath (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f14f9f2d028bb8a9a8e71bc9d7b97ea5672466f1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717628"
---
# <a name="dbengineinipath-property-dao"></a><span data-ttu-id="e07d0-102">Propriété DBEngine.IniPath (DAO)</span><span class="sxs-lookup"><span data-stu-id="e07d0-102">DBEngine.IniPath property (DAO)</span></span>


<span data-ttu-id="e07d0-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e07d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e07d0-104">Définit ou renvoie des informations sur la clé du Registre Windows contenant les valeurs relatives au moteur de base de données Microsoft Access (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="e07d0-104">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="e07d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e07d0-105">Syntax</span></span>

<span data-ttu-id="e07d0-106">*expression* . IniPath</span><span class="sxs-lookup"><span data-stu-id="e07d0-106">*expression* .IniPath</span></span>

<span data-ttu-id="e07d0-107">*expression* Variable qui représente un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="e07d0-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e07d0-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="e07d0-108">Remarks</span></span>

<span data-ttu-id="e07d0-109">Vous pouvez configurer le moteur de base de données Microsoft Access dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="e07d0-109">You can configure the Microsoft Access database engine with the Windows Registry.</span></span> <span data-ttu-id="e07d0-110">Ce dernier permet de définir des options comme les DLL ISAM installables.</span><span class="sxs-lookup"><span data-stu-id="e07d0-110">You can use the Registry to set options, such as installable ISAM DLLs.</span></span>

<span data-ttu-id="e07d0-p102">Pour que cette option soit efficace, vous devez définir la propriété **IniPath** avant que votre application n'invoque un autre code DAO. L'étendue de ce paramètre est limitée à votre application et ne peut pas être modifiée sans redémarrer votre application.</span><span class="sxs-lookup"><span data-stu-id="e07d0-p102">For this option to have any effect, you must set the **IniPath** property before your application invokes any other DAO code. The scope of this setting is limited to your application and can't be changed without restarting your application.</span></span>

<span data-ttu-id="e07d0-p103">Le Registre permet de fournir des paramètres d'initialisation pour certains pilotes de base de données ISAM installables. Par exemple, pour utiliser Paradox version 4.0, définissez la propriété **IniPath** sur une partie du Registre qui contient les paramètres appropriés.</span><span class="sxs-lookup"><span data-stu-id="e07d0-p103">You also use the Registry to provide initialization parameters for some installable ISAM database drivers. For example, to use Paradox version 4.0, set the **IniPath** property to a part of the Registry containing the appropriate parameters.</span></span>

<span data-ttu-id="e07d0-115">Cette propriété reconnaît soit HKEY\_LOCAL\_MACHINE ou HKEY\_LOCAL\_utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e07d0-115">This property recognizes either HKEY\_LOCAL\_MACHINE or HKEY\_LOCAL\_USER.</span></span> <span data-ttu-id="e07d0-116">Si aucune clé racine n’est fourni, la valeur par défaut est HKEY\_LOCAL\_MACHINE.</span><span class="sxs-lookup"><span data-stu-id="e07d0-116">If no root key is supplied, the default is HKEY\_LOCAL\_MACHINE.</span></span>

