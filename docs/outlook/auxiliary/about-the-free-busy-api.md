---
title: À propos de l’API et de disponibilité
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: L’API de disponibilité permet de fournisseurs de messagerie fournir des informations de disponibilité pour les comptes d’utilisateur spécifié au sein d’une plage de temps spécifié.
ms.openlocfilehash: 8b1559173297fbde9930b6f8f7fbc74f176273da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782546"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="59c5e-103">À propos de l’API et de disponibilité</span><span class="sxs-lookup"><span data-stu-id="59c5e-103">About the Free/Busy API</span></span>

<span data-ttu-id="59c5e-104">L’API de disponibilité permet de fournisseurs de messagerie fournir des informations de disponibilité pour les comptes d’utilisateur spécifié au sein d’une plage de temps spécifié.</span><span class="sxs-lookup"><span data-stu-id="59c5e-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="59c5e-105">L’état de disponibilité d’un bloc de temps sur le calendrier d’un utilisateur est une des opérations suivantes : hors du bureau, occupé (e), provisoire ou libre.</span><span class="sxs-lookup"><span data-stu-id="59c5e-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="59c5e-106">Créer un fournisseur et de disponibilité</span><span class="sxs-lookup"><span data-stu-id="59c5e-106">Create a free/busy provider</span></span>

<span data-ttu-id="59c5e-107">Pour fournir des informations de disponibilité pour les utilisateurs de messagerie, un fournisseur de messagerie crée un fournisseur et de disponibilité et l’enregistre avec Outlook.</span><span class="sxs-lookup"><span data-stu-id="59c5e-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="59c5e-108">Le fournisseur et de disponibilité doit implémenter les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="59c5e-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="59c5e-109">Notez qu’un nombre de membres de ces interfaces n’est pas pris en charge et doit renvoyer que les valeurs de retour spécifié.</span><span class="sxs-lookup"><span data-stu-id="59c5e-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="59c5e-110">En particulier, l’API de disponibilité ne gère pas un accès en écriture pour les informations de disponibilité et de déléguer l’accès aux comptes.</span><span class="sxs-lookup"><span data-stu-id="59c5e-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="59c5e-111">[IFreeBusySupport](ifreebusysupport.md) — cette interface prend en charge la spécification des interfaces qui accèdent aux données de disponibilité pour les utilisateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="59c5e-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="59c5e-112">Il utilise [FBUser](fbuser.md) pour identifier un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="59c5e-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="59c5e-113">[IFreeBusyData](ifreebusydata.md) — cette interface obtient et définit une plage de temps pour un utilisateur donné et retourne une interface pour énumérer les informations de disponibilité des blocs de données dans cette plage de temps.</span><span class="sxs-lookup"><span data-stu-id="59c5e-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="59c5e-114">Il utilise une heure relative pour obtenir et définir ce laps de temps.</span><span class="sxs-lookup"><span data-stu-id="59c5e-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="59c5e-115">Pour plus d’informations, voir [heure relative utilisés pour accéder aux données et de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="59c5e-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="59c5e-116">[IEnumFBBlock](ienumfbblock.md) — cette interface prend en charge l’accès et l’énumération des informations de disponibilité des blocs de données pour un utilisateur au sein d’une plage de temps.</span><span class="sxs-lookup"><span data-stu-id="59c5e-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="59c5e-117">Une énumération contient des blocs de disponibilité qui indiquent l’état de disponibilité de périodes de temps dans le calendrier d’un utilisateur, au sein d’une plage de temps (spécifié par [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span><span class="sxs-lookup"><span data-stu-id="59c5e-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="59c5e-118">Éléments dans un calendrier, tels que des rendez-vous et des demandes de réunion, de blocs de forment dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="59c5e-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="59c5e-119">Éléments à côté de l’autre dans le calendrier et ont le même statut de disponibilité sont combinées à former un bloc unique.</span><span class="sxs-lookup"><span data-stu-id="59c5e-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="59c5e-120">Une période de temps dans un calendrier libre forms également un bloc.</span><span class="sxs-lookup"><span data-stu-id="59c5e-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="59c5e-121">Par conséquent, aucune deux blocs consécutifs dans une énumération n’aurait le même état libre/occupé.</span><span class="sxs-lookup"><span data-stu-id="59c5e-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="59c5e-122">Ces blocs ne se chevauchent pas dans le temps.</span><span class="sxs-lookup"><span data-stu-id="59c5e-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="59c5e-123">Lorsqu’il existe des éléments qui se chevauchent dans un calendrier, Outlook fusionne ces éléments pour former des blocs de disponibilité sans chevauchement de l’énumération basée sur cet ordre de priorité : hors du bureau, provisoire, occupé (e).</span><span class="sxs-lookup"><span data-stu-id="59c5e-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="59c5e-124">Pour enregistrer le fournisseur et de disponibilité avec Outlook, le fournisseur de messagerie doit procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="59c5e-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="59c5e-125">Enregistrez le fournisseur et de disponibilité avec COM, en fournissant un CLSID qui autorise l’accès à l’implémentation du fournisseur de **IFreeBusySupport**.</span><span class="sxs-lookup"><span data-stu-id="59c5e-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="59c5e-126">Informer Outlook que le fournisseur et de disponibilité existe en définissant la clé suivante (où `<xx.x>` représente la version d’Outlook) dans le Registre système :</span><span class="sxs-lookup"><span data-stu-id="59c5e-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="59c5e-127">Par exemple, si le fournisseur de transport est SMTP, pour enregistrer le fournisseur avec Microsoft Outlook 2010, définissez la clé suivante pour les données dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="59c5e-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="59c5e-128">Name</span><span class="sxs-lookup"><span data-stu-id="59c5e-128">Name</span></span> |<span data-ttu-id="59c5e-129">Type</span><span class="sxs-lookup"><span data-stu-id="59c5e-129">Type</span></span> |<span data-ttu-id="59c5e-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="59c5e-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="59c5e-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="59c5e-131">SMTP</span></span>  |<span data-ttu-id="59c5e-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="59c5e-132">REG_SZ</span></span>  |<span data-ttu-id="59c5e-133">{CLSID d’implémentation respectif de IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="59c5e-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="59c5e-134">Dans ce scénario, Outlook crée la classe COM et l’utilise pour récupérer des informations de disponibilité pour les utilisateurs de messagerie SMTP.</span><span class="sxs-lookup"><span data-stu-id="59c5e-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="59c5e-135">Pour prendre en charge un fournisseur de transport et le carnet d’adresses qui utilisent un type autre que SMTP entrée d’adresse, modifiez le *nom* en conséquence.</span><span class="sxs-lookup"><span data-stu-id="59c5e-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="59c5e-136">Pendant l’installation, les fournisseurs et de disponibilité doivent vérifier si un paramètre de Registre pour le même type entrée existe déjà.</span><span class="sxs-lookup"><span data-stu-id="59c5e-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="59c5e-137">Si c’est le cas, le fournisseur et de disponibilité doit remplacer le fournisseur en cours pour ce type de l’entrée d’adresse et restaurer à ce fournisseur lors de la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="59c5e-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="59c5e-138">Toutefois, si un utilisateur a installé plusieurs fournisseurs et de disponibilité pour le même type de l’entrée d’adresse, l’utilisateur doit désinstaller ces fournisseurs dans l’ordre inverse en tant que l’installation (autrement dit, désinstallez toujours le fournisseur le plus récent).</span><span class="sxs-lookup"><span data-stu-id="59c5e-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="59c5e-139">Dans le cas contraire, le Registre peut pointer vers un fournisseur qui a déjà été désinstallé.</span><span class="sxs-lookup"><span data-stu-id="59c5e-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="59c5e-140">Composants de l’API</span><span class="sxs-lookup"><span data-stu-id="59c5e-140">API components</span></span>

<span data-ttu-id="59c5e-141">L’API de disponibilité comprend les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="59c5e-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="59c5e-142">Définitions</span><span class="sxs-lookup"><span data-stu-id="59c5e-142">Definitions</span></span>

- [<span data-ttu-id="59c5e-143">Constantes (disponibilité API)</span><span class="sxs-lookup"><span data-stu-id="59c5e-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="59c5e-144">Types de données</span><span class="sxs-lookup"><span data-stu-id="59c5e-144">Data types</span></span>

- [<span data-ttu-id="59c5e-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="59c5e-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="59c5e-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="59c5e-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="59c5e-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="59c5e-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="59c5e-148">Interfaces</span><span class="sxs-lookup"><span data-stu-id="59c5e-148">Interfaces</span></span>

- [<span data-ttu-id="59c5e-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="59c5e-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="59c5e-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="59c5e-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="59c5e-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="59c5e-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

