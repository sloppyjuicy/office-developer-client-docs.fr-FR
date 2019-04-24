---
title: À propos de l’API Disponibilité
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: L'API de disponibilité permet aux fournisseurs de messagerie de fournir des informations de disponibilité pour les comptes d'utilisateurs spécifiés dans un intervalle de temps spécifié.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317009"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="748d7-103">À propos de l’API Disponibilité</span><span class="sxs-lookup"><span data-stu-id="748d7-103">About the Free/Busy API</span></span>

<span data-ttu-id="748d7-104">L'API de disponibilité permet aux fournisseurs de messagerie de fournir des informations de disponibilité pour les comptes d'utilisateurs spécifiés dans un intervalle de temps spécifié.</span><span class="sxs-lookup"><span data-stu-id="748d7-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="748d7-105">L'état de disponibilité d'une plage de temps sur le calendrier d'un utilisateur est l'un des suivants: absent (e) du bureau, inactif, provisoire ou gratuit.</span><span class="sxs-lookup"><span data-stu-id="748d7-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="748d7-106">Créer un fournisseur de disponibilité</span><span class="sxs-lookup"><span data-stu-id="748d7-106">Create a free/busy provider</span></span>

<span data-ttu-id="748d7-107">Pour fournir des informations de disponibilité aux utilisateurs de messagerie, un fournisseur de messagerie crée un fournisseur de disponibilité et l'enregistre auprès d'Outlook.</span><span class="sxs-lookup"><span data-stu-id="748d7-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="748d7-108">Le fournisseur de disponibilité doit implémenter les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="748d7-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="748d7-109">Notez qu'un certain nombre de membres dans ces interfaces ne sont pas pris en charge et doivent renvoyer les valeurs renvoyées spécifiées.</span><span class="sxs-lookup"><span data-stu-id="748d7-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="748d7-110">En particulier, l'API de disponibilité ne prend pas en charge l'accès en écriture aux informations de disponibilité et l'accès délégué aux comptes.</span><span class="sxs-lookup"><span data-stu-id="748d7-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="748d7-111">[IFreeBusySupport](ifreebusysupport.md) : cette interface prend en charge la spécification des interfaces qui accèdent aux données de disponibilité pour les utilisateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="748d7-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="748d7-112">Il utilise [FBUser](fbuser.md) pour identifier un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="748d7-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="748d7-113">[IFreeBusyData](ifreebusydata.md) : cette interface obtient et définit une plage horaire pour un utilisateur donné et retourne une interface pour l'énumération des blocs de données de disponibilité dans cette plage de temps.</span><span class="sxs-lookup"><span data-stu-id="748d7-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="748d7-114">Il utilise l'heure relative pour obtenir et définir ce intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="748d7-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="748d7-115">Pour plus d'informations, consultez la rubrique [utilisation de l'heure relative pour accéder aux données de](how-to-use-relative-time-to-access-free-busy-data.md)disponibilité.</span><span class="sxs-lookup"><span data-stu-id="748d7-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="748d7-116">[IEnumFBBlock](ienumfbblock.md) : cette interface prend en charge l'accès et l'énumération des blocs de données de disponibilité d'un utilisateur dans un intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="748d7-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="748d7-117">Une énumération contient des blocs de disponibilité qui indiquent l'état de disponibilité des périodes sur le calendrier d'un utilisateur, dans un intervalle de temps (spécifié par [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md)).</span><span class="sxs-lookup"><span data-stu-id="748d7-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="748d7-118">Éléments d'un calendrier, tels que les rendez-vous et les demandes de réunion, les blocs de formulaire dans l'énumération.</span><span class="sxs-lookup"><span data-stu-id="748d7-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="748d7-119">Les éléments adjacents les uns aux autres sur le calendrier et qui ont le même état de disponibilité sont combinés pour former un seul bloc.</span><span class="sxs-lookup"><span data-stu-id="748d7-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="748d7-120">Une période de temps libre sur un calendrier forme également un bloc.</span><span class="sxs-lookup"><span data-stu-id="748d7-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="748d7-121">Par conséquent, deux blocs consécutifs dans une énumération ne peuvent pas avoir le même état de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="748d7-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="748d7-122">Ces blocs ne se chevauchent pas dans le temps.</span><span class="sxs-lookup"><span data-stu-id="748d7-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="748d7-123">Lorsqu'il y a des éléments qui se chevauchent dans un calendrier, Outlook fusionne ces éléments pour créer des blocs de disponibilité qui ne se chevauchent pas dans l'énumération en fonction de cet ordre de priorité: absent (e) du bureau, occupé (e).</span><span class="sxs-lookup"><span data-stu-id="748d7-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="748d7-124">Pour enregistrer le fournisseur de disponibilité auprès d'Outlook, le fournisseur de messagerie doit effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="748d7-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="748d7-125">Inscrivez le fournisseur de disponibilité à l'aide de COM, en fournissant un CLSID qui permet d'accéder à l'implémentation du fournisseur de **IFreeBusySupport**.</span><span class="sxs-lookup"><span data-stu-id="748d7-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="748d7-126">Indiquez à Outlook que le fournisseur de disponibilité existe en définissant la clé suivante (où `<xx.x>` correspond à la version d'Outlook) dans le registre système:</span><span class="sxs-lookup"><span data-stu-id="748d7-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="748d7-127">Par exemple, si le fournisseur de transport est SMTP, pour enregistrer le fournisseur avec Microsoft Outlook 2010, définissez la clé suivante sur les données dans le tableau suivant:</span><span class="sxs-lookup"><span data-stu-id="748d7-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="748d7-128">Nom</span><span class="sxs-lookup"><span data-stu-id="748d7-128">Name</span></span> |<span data-ttu-id="748d7-129">Type</span><span class="sxs-lookup"><span data-stu-id="748d7-129">Type</span></span> |<span data-ttu-id="748d7-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="748d7-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="748d7-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="748d7-131">SMTP</span></span>  |<span data-ttu-id="748d7-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="748d7-132">REG_SZ</span></span>  |<span data-ttu-id="748d7-133">{CLSID pour la mise en œuvre respective de IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="748d7-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="748d7-134">Dans ce scénario, Outlook co-crée la classe COM et l'utilise pour récupérer des informations de disponibilité pour les utilisateurs de messagerie SMTP.</span><span class="sxs-lookup"><span data-stu-id="748d7-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="748d7-135">Pour prendre en charge un carnet d'adresses et un fournisseur de transport qui utilisent un type d'entrée d'adresse autre que SMTP, modifiez le *nom* en conséquence.</span><span class="sxs-lookup"><span data-stu-id="748d7-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="748d7-136">Pendant l'installation, les fournisseurs de disponibilité doivent vérifier si un paramètre de Registre pour le même type d'entrée d'adresse existe déjà.</span><span class="sxs-lookup"><span data-stu-id="748d7-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="748d7-137">Si c'est le cas, le fournisseur de disponibilité doit remplacer le fournisseur actuel pour ce type d'entrée d'adresse et effectuer la restauration auprès de ce fournisseur lors de la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="748d7-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="748d7-138">Toutefois, si un utilisateur a installé plus d'un fournisseur de disponibilité pour le même type d'entrée d'adresse, l'utilisateur doit désinstaller ces fournisseurs dans l'ordre inverse en tant qu'installation (c'est-à-dire, toujours désinstaller le dernier fournisseur).</span><span class="sxs-lookup"><span data-stu-id="748d7-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="748d7-139">Dans le cas contraire, le registre peut pointer vers un fournisseur qui a déjà été désinstallé.</span><span class="sxs-lookup"><span data-stu-id="748d7-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="748d7-140">Composants de l'API</span><span class="sxs-lookup"><span data-stu-id="748d7-140">API components</span></span>

<span data-ttu-id="748d7-141">L'API de disponibilité inclut les composants suivants:</span><span class="sxs-lookup"><span data-stu-id="748d7-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="748d7-142">Définitions</span><span class="sxs-lookup"><span data-stu-id="748d7-142">Definitions</span></span>

- [<span data-ttu-id="748d7-143">Constantes (API de disponibilité)</span><span class="sxs-lookup"><span data-stu-id="748d7-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="748d7-144">Types de données</span><span class="sxs-lookup"><span data-stu-id="748d7-144">Data types</span></span>

- [<span data-ttu-id="748d7-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="748d7-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="748d7-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="748d7-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="748d7-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="748d7-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="748d7-148">Interfaces</span><span class="sxs-lookup"><span data-stu-id="748d7-148">Interfaces</span></span>

- [<span data-ttu-id="748d7-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="748d7-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="748d7-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="748d7-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="748d7-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="748d7-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

