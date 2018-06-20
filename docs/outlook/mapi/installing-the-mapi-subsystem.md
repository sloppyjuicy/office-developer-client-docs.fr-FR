---
title: Installation du sous-système MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c2e135fc031dd3faf5a4e08c50147dfcf7787b5e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784316"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="b792f-103">Installation du sous-système MAPI</span><span class="sxs-lookup"><span data-stu-id="b792f-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="b792f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b792f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b792f-105">Versions prises en charge de Windows installent la bibliothèque stub MAPI, Mapi32.dll, dans le _ \<lecteur\>_ dossier \Windows\System32.</span><span class="sxs-lookup"><span data-stu-id="b792f-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="b792f-106">Les versions de Windows prises en charge sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b792f-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="b792f-107">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b792f-107">Windows 7.</span></span>
    
- <span data-ttu-id="b792f-108">Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b792f-108">Windows Vista.</span></span>
    
- <span data-ttu-id="b792f-109">Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b792f-109">Windows Server 2008.</span></span>
    
- <span data-ttu-id="b792f-110">Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b792f-110">Windows Server 2003.</span></span>
    
- <span data-ttu-id="b792f-111">Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b792f-111">Windows XP.</span></span>
    
<span data-ttu-id="b792f-112">Pour installer correctement le sous-système MAPI, installer une application qui contient un sous-système basées sur MAPI, tel que Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="b792f-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="b792f-113">Vous trouverez plus d’informations sur l’installation du sous-système MAPI d’un ordinateur dans le Registre système.</span><span class="sxs-lookup"><span data-stu-id="b792f-113">You can find information about a computer's MAPI subsystem installation in the system registry.</span></span> <span data-ttu-id="b792f-114">Toutes les valeurs dans les entrées de Registre sont des chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="b792f-114">All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="b792f-115">Programmes d’installation de service de message sont chargés de créer les informations d’installation dans la clé de Registre système suivantes :</span><span class="sxs-lookup"><span data-stu-id="b792f-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="b792f-116">Services de messagerie doivent ajouter des entrées dans le Registre système.</span><span class="sxs-lookup"><span data-stu-id="b792f-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="b792f-117">Le tableau suivant résume comment les clients récupèrent les informations de version pour le sous-système MAPI sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b792f-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="b792f-118">**Pour vérifier**</span><span class="sxs-lookup"><span data-stu-id="b792f-118">**To check**</span></span>|<span data-ttu-id="b792f-119">**Dans le Registre**</span><span class="sxs-lookup"><span data-stu-id="b792f-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b792f-120">Disponibilité de MAPI</span><span class="sxs-lookup"><span data-stu-id="b792f-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="b792f-121">Recherchez `MAPIX=1`.</span><span class="sxs-lookup"><span data-stu-id="b792f-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="b792f-122">Version de MAPI</span><span class="sxs-lookup"><span data-stu-id="b792f-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="b792f-123">Rechercher une chaîne MAPIXVER sous la forme « _x.x.x_».</span><span class="sxs-lookup"><span data-stu-id="b792f-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b792f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b792f-124">See also</span></span>



[<span data-ttu-id="b792f-125">Vue d'ensemble de la programmation MAPI</span><span class="sxs-lookup"><span data-stu-id="b792f-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

