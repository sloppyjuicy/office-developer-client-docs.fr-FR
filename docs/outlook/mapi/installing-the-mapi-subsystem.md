---
title: Installation du sous-système MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: Dernière modification le 9 mars 2015
localization_priority: Priority
ms.openlocfilehash: 112a683f5967f8740c2d21285eb4ebbc0f455c48
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722437"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="32930-103">Installation du sous-système MAPI</span><span class="sxs-lookup"><span data-stu-id="32930-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="32930-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32930-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32930-105">Les versions prises en charge de Windows installent la bibliothèque stub MAPI, Mapi32.dll, dans le dossier _\<drive\>_ \Windows\System32.</span><span class="sxs-lookup"><span data-stu-id="32930-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="32930-106">Voici les versions prises en charge de Windows :</span><span class="sxs-lookup"><span data-stu-id="32930-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="32930-107">Windows 7</span><span class="sxs-lookup"><span data-stu-id="32930-107">Windows 7</span></span>
    
- <span data-ttu-id="32930-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32930-108">Windows Vista</span></span>
    
- <span data-ttu-id="32930-109">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32930-109">Windows Server 2008</span></span>
    
- <span data-ttu-id="32930-110">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="32930-110">Windows Server 2003</span></span>
    
- <span data-ttu-id="32930-111">Windows XP</span><span class="sxs-lookup"><span data-stu-id="32930-111">Windows XP</span></span>
    
<span data-ttu-id="32930-112">Pour installer correctement le sous-système MAPI, installez une application qui contient un sous-système de MAPI, tel que Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="32930-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="32930-113">Vous trouverez des informations sur l’installation du sous-système MAPI d’un ordinateur dans le Registre système.</span><span class="sxs-lookup"><span data-stu-id="32930-113">You can find information about a computer's MAPI subsystem installation in the system registry.</span></span> <span data-ttu-id="32930-114">Toutes les valeurs indiquées dans les entrées du registre sont des chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="32930-114">All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="32930-115">Les programmes d’installation de service de messagerie sont chargés de créer les informations d’installation dans la clé du Registre système suivante :</span><span class="sxs-lookup"><span data-stu-id="32930-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="32930-116">Les services de messagerie doivent ajouter des entrées au Registre système.</span><span class="sxs-lookup"><span data-stu-id="32930-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="32930-117">Le tableau suivant récapitule comment les clients récupèrent les informations de version pour le sous-système MAPI sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="32930-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="32930-118">**Pour vérifier**</span><span class="sxs-lookup"><span data-stu-id="32930-118">**To check**</span></span>|<span data-ttu-id="32930-119">**Registre**</span><span class="sxs-lookup"><span data-stu-id="32930-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32930-120">Disponibilité de MAPI</span><span class="sxs-lookup"><span data-stu-id="32930-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="32930-121">Rechercher `MAPIX=1`.</span><span class="sxs-lookup"><span data-stu-id="32930-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="32930-122">Version disponible de MAPI</span><span class="sxs-lookup"><span data-stu-id="32930-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="32930-123">Rechercher une chaîne MAPIXVER au format « _x.x.x_ ».</span><span class="sxs-lookup"><span data-stu-id="32930-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32930-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32930-124">See also</span></span>



[<span data-ttu-id="32930-125">Vue d’ensemble de la programmation MAPI</span><span class="sxs-lookup"><span data-stu-id="32930-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

