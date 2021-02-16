---
title: À propos de l’API Disponibilité
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: L’API de libre/occupé permet aux fournisseurs de messagerie de fournir des informations d’état de libre/occupé pour les comptes d’utilisateur spécifiés dans un délai spécifié.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433758"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="0157a-103">À propos de l’API Disponibilité</span><span class="sxs-lookup"><span data-stu-id="0157a-103">About the Free/Busy API</span></span>

<span data-ttu-id="0157a-104">L’API de libre/occupé permet aux fournisseurs de messagerie de fournir des informations d’état de libre/occupé pour les comptes d’utilisateur spécifiés dans un délai spécifié.</span><span class="sxs-lookup"><span data-stu-id="0157a-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="0157a-105">L’état de libre/occupé d’un bloc de temps dans le calendrier d’un utilisateur est l’un des suivants : in-office, occupé, provisoire ou gratuit.</span><span class="sxs-lookup"><span data-stu-id="0157a-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="0157a-106">Créer un fournisseur de services de libre-service</span><span class="sxs-lookup"><span data-stu-id="0157a-106">Create a free/busy provider</span></span>

<span data-ttu-id="0157a-107">Pour fournir des informations de libre/occupé aux utilisateurs de messagerie, un fournisseur de messagerie crée un fournisseur de libre/occupé et l’inscrit auprès d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="0157a-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="0157a-108">Le fournisseur de libre/occupé doit implémenter les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="0157a-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="0157a-109">Notez qu’un certain nombre de membres dans ces interfaces ne sont pas pris en charge et doivent renvoyer les valeurs de retour spécifiées.</span><span class="sxs-lookup"><span data-stu-id="0157a-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="0157a-110">En particulier, l’API de libre/occupé ne prend pas en charge l’accès en écriture aux informations de libre/occupé et déléguer l’accès aux comptes.</span><span class="sxs-lookup"><span data-stu-id="0157a-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="0157a-111">[IFreeBusySupport](ifreebusysupport.md) : cette interface prend en charge la spécification des interfaces qui accèdent aux données de libre/occupé pour les utilisateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0157a-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="0157a-112">Il utilise [FBUser pour](fbuser.md) identifier un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0157a-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="0157a-113">[IFreeBusyData](ifreebusydata.md) — Cette interface obtient et définit une plage de temps pour un utilisateur donné et renvoie une interface pour l’éumation des blocs de données de libre/occupé dans cette plage de temps.</span><span class="sxs-lookup"><span data-stu-id="0157a-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="0157a-114">Il utilise le temps relatif pour obtenir et définir cette plage de temps.</span><span class="sxs-lookup"><span data-stu-id="0157a-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="0157a-115">Pour plus d’informations, voir [Utiliser l’heure relative pour accéder aux données de libre/occupé.](how-to-use-relative-time-to-access-free-busy-data.md)</span><span class="sxs-lookup"><span data-stu-id="0157a-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="0157a-116">[IEnumFBBlock —](ienumfbblock.md) Cette interface prend en charge l’accès et l’éumation des blocs de données de la période de libre/occupé d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0157a-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="0157a-117">Une éumération contient des blocs de libre/occupé qui indiquent l’état de la période de libre/occupé du calendrier d’un utilisateur, dans une plage de temps (spécifiée par [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span><span class="sxs-lookup"><span data-stu-id="0157a-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="0157a-118">Éléments d’un calendrier, tels que les rendez-vous et les demandes de réunion, blocs de formulaire dans l’éumération.</span><span class="sxs-lookup"><span data-stu-id="0157a-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="0157a-119">Les éléments qui sont adjacents les uns aux autres sur le calendrier et qui ont le même statut de libre/occupé sont combinés pour former un seul bloc.</span><span class="sxs-lookup"><span data-stu-id="0157a-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="0157a-120">Une période gratuite sur un calendrier constitue également un bloc.</span><span class="sxs-lookup"><span data-stu-id="0157a-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="0157a-121">Par conséquent, deux blocs consécutifs dans une éumération n’auraient pas le même statut de libre/occupé.</span><span class="sxs-lookup"><span data-stu-id="0157a-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="0157a-122">Ces blocs ne se chevauchent pas dans le temps.</span><span class="sxs-lookup"><span data-stu-id="0157a-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="0157a-123">Lorsqu’un calendrier se chevauche, Outlook fusionne ces éléments pour former des blocs de libre/occupé non superposés dans l’éumération en fonction de cet ordre de priorité : absence du bureau, occupé, provisoire.</span><span class="sxs-lookup"><span data-stu-id="0157a-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="0157a-124">Pour inscrire le fournisseur de libre/occupé auprès d’Outlook, le fournisseur de messagerie doit :</span><span class="sxs-lookup"><span data-stu-id="0157a-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="0157a-125">Inscrivez le fournisseur de libre/occupé auprès de COM, en fournissant un CLSID qui permet d’accéder à l’implémentation du fournisseur **de IFreeBusySupport**.</span><span class="sxs-lookup"><span data-stu-id="0157a-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="0157a-126">Faites savoir à Outlook que le fournisseur de services de libre-service existe en fixant la clé suivante (où représente la version d’Outlook) dans le Registre `<xx.x>` système :</span><span class="sxs-lookup"><span data-stu-id="0157a-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="0157a-127">Par exemple, si le fournisseur de transport est SMTP, pour enregistrer le fournisseur auprès de Microsoft Outlook 2010, définissez la clé suivante sur les données du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="0157a-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="0157a-128">Nom</span><span class="sxs-lookup"><span data-stu-id="0157a-128">Name</span></span> |<span data-ttu-id="0157a-129">Type</span><span class="sxs-lookup"><span data-stu-id="0157a-129">Type</span></span> |<span data-ttu-id="0157a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="0157a-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="0157a-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="0157a-131">SMTP</span></span>  |<span data-ttu-id="0157a-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0157a-132">REG_SZ</span></span>  |<span data-ttu-id="0157a-133">{CLSID pour l’implémentation respective d’IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="0157a-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="0157a-134">Dans ce scénario, Outlook co-crée la classe COM et l’utilise pour récupérer des informations de libre/occupé pour tous les utilisateurs de messagerie SMTP.</span><span class="sxs-lookup"><span data-stu-id="0157a-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="0157a-135">Pour prendre en charge un carnet d’adresses et un fournisseur de transport qui utilisent un type d’entrée d’adresse autre que SMTP, modifiez  *le* nom en conséquence.</span><span class="sxs-lookup"><span data-stu-id="0157a-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0157a-136">Pendant l’installation, les fournisseurs de services de libre-service doivent vérifier si un paramètre de Registre pour le même type d’entrée d’adresse existe déjà.</span><span class="sxs-lookup"><span data-stu-id="0157a-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="0157a-137">Si c’est le cas, le fournisseur de libre/occupé doit le faire pour ce type d’entrée d’adresse et le restaurer lors de sa désinstallation.</span><span class="sxs-lookup"><span data-stu-id="0157a-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="0157a-138">Toutefois, si un utilisateur a installé plusieurs fournisseurs de libre/occupé pour le même type d’entrée d’adresse, il doit désinstaller ces fournisseurs dans l’ordre inverse en tant qu’installation (autrement dit, désinstaller toujours le dernier fournisseur).</span><span class="sxs-lookup"><span data-stu-id="0157a-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="0157a-139">Sinon, le Registre peut pointer vers un fournisseur qui a déjà été désinstallé.</span><span class="sxs-lookup"><span data-stu-id="0157a-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="0157a-140">Composants d’API</span><span class="sxs-lookup"><span data-stu-id="0157a-140">API components</span></span>

<span data-ttu-id="0157a-141">L’API de libre/occupé inclut les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="0157a-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="0157a-142">Définitions</span><span class="sxs-lookup"><span data-stu-id="0157a-142">Definitions</span></span>

- [<span data-ttu-id="0157a-143">Constantes (API de libre/occupé)</span><span class="sxs-lookup"><span data-stu-id="0157a-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="0157a-144">Types de données</span><span class="sxs-lookup"><span data-stu-id="0157a-144">Data types</span></span>

- [<span data-ttu-id="0157a-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="0157a-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="0157a-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="0157a-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="0157a-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="0157a-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="0157a-148">Interfaces</span><span class="sxs-lookup"><span data-stu-id="0157a-148">Interfaces</span></span>

- [<span data-ttu-id="0157a-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="0157a-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="0157a-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="0157a-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="0157a-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="0157a-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

