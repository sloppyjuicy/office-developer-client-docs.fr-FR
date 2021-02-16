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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316428"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="87c22-103">Propriété canonique PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="87c22-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="87c22-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87c22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87c22-105">Contient un GUID généré dynamiquement utilisé pour déterminer un compte lorsque vous utilisez plusieurs Microsoft Exchange Server comptes.</span><span class="sxs-lookup"><span data-stu-id="87c22-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87c22-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="87c22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87c22-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="87c22-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="87c22-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="87c22-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87c22-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="87c22-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="87c22-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="87c22-110">Data type:</span></span>  <br/> |<span data-ttu-id="87c22-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="87c22-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="87c22-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="87c22-112">Area:</span></span>  <br/> |<span data-ttu-id="87c22-113">Comptes Exchange multiples</span><span class="sxs-lookup"><span data-stu-id="87c22-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87c22-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="87c22-114">Remarks</span></span>

<span data-ttu-id="87c22-115">Microsoft Outlook 2010 et Microsoft Outlook 2013 peuvent prendre en charge plusieurs comptes Exchange au lieu d’un seul.</span><span class="sxs-lookup"><span data-stu-id="87c22-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="87c22-116">Pour prendre en charge plusieurs comptes Exchange, la disposition du profil MAPI a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="87c22-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="87c22-117">Dans Microsoft Office Outlook 2007 et les précédentes, les profils contenaient une section de profil fixe dédiée aux paramètres Exchange tels que le nom du serveur, le nom d’utilisateur et le fichier de dossier hors connexion (.ost).</span><span class="sxs-lookup"><span data-stu-id="87c22-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="87c22-118">emplacement.</span><span class="sxs-lookup"><span data-stu-id="87c22-118">location.</span></span> <span data-ttu-id="87c22-119">Ces paramètres ont été identifiés à l’aide d’un identificateur unique, la **propriété pbGlobalProfileSectionGuid.**</span><span class="sxs-lookup"><span data-stu-id="87c22-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="87c22-120">La section utilisée pour les paramètres Exchange est appelée section Profil global Exchange.</span><span class="sxs-lookup"><span data-stu-id="87c22-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> 
  
<span data-ttu-id="87c22-121">Un emplacement de section de profil fixe ne suffit plus pour prendre en charge plusieurs comptes Exchange.</span><span class="sxs-lookup"><span data-stu-id="87c22-121">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="87c22-122">À la place, pour chaque compte Exchange de votre profil, il existe une section dédiée aux paramètres de ce compte.</span><span class="sxs-lookup"><span data-stu-id="87c22-122">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="87c22-123">La nouvelle section utilisée pour les paramètres Exchange est identifiée par l’identificateur unique **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="87c22-123">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="87c22-124">Dans la section profil de service de message pour le compte Exchange, vous pouvez trouver une propriété qui contient un GUID qui est généré dynamiquement au moment de la création du compte.</span><span class="sxs-lookup"><span data-stu-id="87c22-124">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="87c22-125">Ce GUID est stocké dans la **propriété PidTagExchangeProfileSectionId.**</span><span class="sxs-lookup"><span data-stu-id="87c22-125">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="87c22-126">Les magasins de messages et les conteneurs de carnet d’adresses exposent une propriété pour déterminer le compte Exchange auquel ils appartiennent.</span><span class="sxs-lookup"><span data-stu-id="87c22-126">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="87c22-127">Accessible dans la table des services de message, chaque service Exchange expose cette propriété.</span><span class="sxs-lookup"><span data-stu-id="87c22-127">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="87c22-128">Vous pouvez récupérer cette propriété via un appel à [IMAPIProp::GetProps](imapiprop-getprops.md) sur **PidTagExchangeProfileSectionId** après avoir fait une requête pour l’une des interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="87c22-128">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="87c22-129">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="87c22-129">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="87c22-130">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="87c22-130">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="87c22-131">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="87c22-131">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="87c22-132">Si l’objet n’est pas affilié à Exchange, l’appel **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="87c22-132">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="87c22-133">Vous pouvez restreindre les conteneurs sur **un pidTagExchangeProfileSectionId** lors de l’affichage du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="87c22-133">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="87c22-134">Une fois que vous avez un conteneur ouvert, vous pouvez interroger **emsmdbUID à** partir de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="87c22-134">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="87c22-135">Il est également intéressant de noter que si un destinataire a été sélectionné dans un carnet d’adresses Exchange, le destinataire a également le **PidTagExchangeProfileSectionId** dans sa liste de propriétés.</span><span class="sxs-lookup"><span data-stu-id="87c22-135">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="87c22-136">Tout au long des exemples de code et des en-têtes de fonction, ce GUID est appelé **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="87c22-136">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="87c22-137">L’un des comptes Exchange est marqué comme compte Exchange hérité.</span><span class="sxs-lookup"><span data-stu-id="87c22-137">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="87c22-138">En règle générale, il s’agit du premier compte ajouté au profil.</span><span class="sxs-lookup"><span data-stu-id="87c22-138">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="87c22-139">Chaque appel pour **ouvrir pbGlobalProfileSectionGuid** est redirigé vers la section globale Exchange du compte hérité.</span><span class="sxs-lookup"><span data-stu-id="87c22-139">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="87c22-140">Les appels de modèle objet qui interagissent avec le compte Exchange non hérité interagissent également avec le compte Exchange hérité.</span><span class="sxs-lookup"><span data-stu-id="87c22-140">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="87c22-141">Le service Exchange hérité possède la propriété **PR_EMSMDB_LEGACY** (0x3D18000B), qui est définie sur **true** dans la table des services de messages.</span><span class="sxs-lookup"><span data-stu-id="87c22-141">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="87c22-142">**L’emsmdbUID** hérité est également marqué dans la section profil global Outlook du profil en tant que **PidTagExchangeProfileSectionId**.</span><span class="sxs-lookup"><span data-stu-id="87c22-142">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="87c22-143">Le code écrit pour prendre en charge plusieurs comptes Exchange ne doit pas avoir à récupérer **l’emsmdbUID** hérité, car il doit obtenir le **emsmdbUID** correct, en fonction du compte avec qui votre code interagit.</span><span class="sxs-lookup"><span data-stu-id="87c22-143">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="87c22-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87c22-144">See also</span></span>



[<span data-ttu-id="87c22-145">Utilisation de plusieurs comptes Exchange</span><span class="sxs-lookup"><span data-stu-id="87c22-145">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


[<span data-ttu-id="87c22-146">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="87c22-146">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

