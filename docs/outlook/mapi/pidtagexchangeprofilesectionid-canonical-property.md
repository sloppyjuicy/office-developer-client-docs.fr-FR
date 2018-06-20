---
title: Propriété canonique PidTagExchangeProfileSectionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 37a318df01101487fe0e8970251201c2515d1e8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785968"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="5d442-103">Propriété canonique PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="5d442-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="5d442-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d442-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d442-105">Contient un GUID généré de manière dynamique permet de déterminer un compte lorsque vous utilisez plusieurs comptes Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5d442-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d442-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5d442-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d442-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="5d442-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="5d442-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5d442-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d442-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="5d442-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="5d442-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5d442-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d442-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5d442-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5d442-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="5d442-112">Area:</span></span>  <br/> |<span data-ttu-id="5d442-113">Comptes Exchange multiples</span><span class="sxs-lookup"><span data-stu-id="5d442-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d442-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5d442-114">Remarks</span></span>

<span data-ttu-id="5d442-115">Microsoft Outlook 2010 et Microsoft Outlook 2013 prend en charge plusieurs comptes Exchange au lieu d’un seul compte Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d442-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="5d442-116">Pour prendre en charge plusieurs comptes Exchange, la mise en page de profil MAPI a été modifié.</span><span class="sxs-lookup"><span data-stu-id="5d442-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="5d442-117">Dans Microsoft Office Outlook 2007 et versions antérieures, profils contenu dans une section de profil fixe dédiée aux paramètres Exchange comme nom du serveur, nom d’utilisateur et le fichier de dossier en mode hors connexion (.ost).</span><span class="sxs-lookup"><span data-stu-id="5d442-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="5d442-118">emplacement.</span><span class="sxs-lookup"><span data-stu-id="5d442-118">location.</span></span> <span data-ttu-id="5d442-119">Ces paramètres ont été identifiés à l’aide d’un identificateur unique de la propriété **pbGlobalProfileSectionGuid** .</span><span class="sxs-lookup"><span data-stu-id="5d442-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="5d442-120">La section utilisée pour les paramètres Exchange est appelée la Section globale Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d442-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> <span data-ttu-id="5d442-121">Pour plus d’informations sur le profil Global Exchange dans Outlook 2007, voir [comment ouvrir la Section profil Global](http://support.microsoft.com/kb/188482).</span><span class="sxs-lookup"><span data-stu-id="5d442-121">For more information about the Exchange Global Profile in Outlook 2007, see [How To Open the Global Profile Section](http://support.microsoft.com/kb/188482).</span></span>
  
<span data-ttu-id="5d442-122">Un emplacement de la section profil fixe n’est plus suffisant pour prendre en charge plusieurs comptes Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d442-122">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="5d442-123">Au lieu de cela, pour chaque compte Exchange dans votre profil, il existe une section consacrée aux paramètres de ce compte.</span><span class="sxs-lookup"><span data-stu-id="5d442-123">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="5d442-124">La nouvelle section utilisée pour les paramètres Exchange est identifiée par l' identificateur unique **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="5d442-124">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="5d442-125">Dans la section de profil de service de message pour le compte Exchange, vous pouvez trouver une propriété qui contient un GUID qui est généré de manière dynamique au moment où le compte est créé.</span><span class="sxs-lookup"><span data-stu-id="5d442-125">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="5d442-126">Ce GUID est stocké dans la propriété **PidTagExchangeProfileSectionId** .</span><span class="sxs-lookup"><span data-stu-id="5d442-126">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="5d442-127">Banques de messages et les conteneurs de carnet d’adresses exposent une propriété pour déterminer quel compte Exchange auxquels ils appartiennent.</span><span class="sxs-lookup"><span data-stu-id="5d442-127">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="5d442-128">Accessibles dans le tableau des services message, chaque service Exchange expose cette propriété.</span><span class="sxs-lookup"><span data-stu-id="5d442-128">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="5d442-129">Vous pouvez extraire cette propriété via un appel à [IMAPIProp::GetProps](imapiprop-getprops.md) sur **PidTagExchangeProfileSectionId** après interrogation pour une des interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="5d442-129">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="5d442-130">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5d442-130">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="5d442-131">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5d442-131">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="5d442-132">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5d442-132">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="5d442-133">Si l’objet n’est pas affilié Exchange, l’appel renvoie **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="5d442-133">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="5d442-134">Vous pouvez restreindre les conteneurs sur un **PidTagExchangeProfileSectionId** lors de l’affichage du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="5d442-134">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="5d442-135">Une fois que vous avez un conteneur ouvert, vous pouvez interroger l' **emsmdbUID** à partir de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="5d442-135">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="5d442-136">Il est également important de noter que si un destinataire a été sélectionné dans un carnet d’adresses de Exchange, le destinataire a également la **PidTagExchangeProfileSectionId** dans sa liste des propriétés.</span><span class="sxs-lookup"><span data-stu-id="5d442-136">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5d442-137">Dans les exemples de code et les en-têtes de fonction, ce GUID est appelé **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="5d442-137">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="5d442-138">Un des comptes Exchange est marqué comme le compte Exchange hérité.</span><span class="sxs-lookup"><span data-stu-id="5d442-138">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="5d442-139">En règle générale, il est le premier compte ajouté au profil.</span><span class="sxs-lookup"><span data-stu-id="5d442-139">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="5d442-140">Chaque appel pour ouvrir **pbGlobalProfileSectionGuid** est redirigé vers la section globale Exchange du compte hérité.</span><span class="sxs-lookup"><span data-stu-id="5d442-140">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="5d442-141">Les appels de modèle objet qui interagissent avec un compte Exchange non héritée également interagissent avec le compte Exchange hérité.</span><span class="sxs-lookup"><span data-stu-id="5d442-141">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="5d442-142">Le service Exchange hérité possède la propriété **PR_EMSMDB_LEGACY** (0x3D18000B), qui est défini sur **true** dans la table des services.</span><span class="sxs-lookup"><span data-stu-id="5d442-142">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="5d442-143">Les anciens **emsmdbUID** est également marqué dans la Section de profil Outlook globale du profil en tant que **PidTagExchangeProfileSectionId**.</span><span class="sxs-lookup"><span data-stu-id="5d442-143">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="5d442-144">Le code écrit pour prendre en charge plusieurs comptes Exchange devront pas récupérer les anciens **emsmdbUID** , car il doit obtenir le correct **emsmdbUID**, selon le compte d’avec que votre code interagit.</span><span class="sxs-lookup"><span data-stu-id="5d442-144">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5d442-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d442-145">See also</span></span>



[<span data-ttu-id="5d442-146">Utilisation de plusieurs comptes Exchange</span><span class="sxs-lookup"><span data-stu-id="5d442-146">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


[<span data-ttu-id="5d442-147">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="5d442-147">How To Open the Global Profile Section</span></span>](http://support.microsoft.com/kb/188482)

