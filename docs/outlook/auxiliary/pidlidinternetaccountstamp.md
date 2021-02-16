---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Renvoie le cachet du compte qui a remis le message.
ms.openlocfilehash: c5da45268cefbe09588fdcfcda32e4e7a4be9d5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327726"
---
# <a name="pidlidinternetaccountstamp"></a><span data-ttu-id="4359e-103">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="4359e-103">PidLidInternetAccountStamp</span></span>

<span data-ttu-id="4359e-104">Renvoie le cachet du compte qui a remis le message.</span><span class="sxs-lookup"><span data-stu-id="4359e-104">Returns the account stamp of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4359e-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="4359e-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4359e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4359e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4359e-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="4359e-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="4359e-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="4359e-108">Property set:</span></span>  <br/> |<span data-ttu-id="4359e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4359e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4359e-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="4359e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4359e-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="4359e-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="4359e-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4359e-112">Data type:</span></span>  <br/> |<span data-ttu-id="4359e-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4359e-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4359e-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4359e-114">Area:</span></span>  <br/> |<span data-ttu-id="4359e-115">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="4359e-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4359e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="4359e-116">Remarks</span></span>

<span data-ttu-id="4359e-117">Cette propriété doit contenir la même valeur que celle renvoyée par la propriété API de gestion des [PROP_ACCT_STAMP](prop_acct_stamp.md) du compte qui a remis le message.</span><span class="sxs-lookup"><span data-stu-id="4359e-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_STAMP](prop_acct_stamp.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="4359e-118">Les fournisseurs de magasins de messages exposent cette propriété nommée et [PidLidInternetAccountName](pidlidinternetaccountname.md) afin que les actions suivantes se produisent :</span><span class="sxs-lookup"><span data-stu-id="4359e-118">Message store providers expose this named property and [PidLidInternetAccountName](pidlidinternetaccountname.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="4359e-119">Lorsqu’un utilisateur clique sur **Répondre** à tous dans un message électronique, Outlook supprime l’adresse de messagerie associée au compte et est inscrite sur le message dans la liste des destinataires de la réponse.</span><span class="sxs-lookup"><span data-stu-id="4359e-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="4359e-120">Ce comportement se produit sauf si cette adresse de messagerie est l’expéditeur du message d’origine.</span><span class="sxs-lookup"><span data-stu-id="4359e-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="4359e-121">Par défaut, Outlook envoie des réponses et des messages transmis via le compte qui est marqué sur le message d’origine.</span><span class="sxs-lookup"><span data-stu-id="4359e-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="4359e-122">Généralement, le Gestionnaire de protocole Outlook fournit des messages et Outlook définit les propriétés **PidLidInternetAccountName** et **PidLidInternetAccountStamp** pour indiquer le compte qui a remis le message.</span><span class="sxs-lookup"><span data-stu-id="4359e-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="4359e-123">Toutefois, si une magasin de messages est étroitement associée à un transport, le Gestionnaire de protocole Outlook ne fournit pas de messages et Outlook ne peut pas définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4359e-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="4359e-124">Dans ce scénario, Outlook appelle la [fonction IMAPIProp::GetIDsFromNames.](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4359e-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="4359e-125">Si le fournisseur de magasin de messages souhaite exposer ces propriétés nommées, il doit implémenter **IMAPIProp::GetIDsFromNames** et renvoyer des balises de propriété via le paramètre de sortie  *lppPropTags*  .</span><span class="sxs-lookup"><span data-stu-id="4359e-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="4359e-126">Outlook peut ensuite appeler la méthode [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) à l’aide de ces balises de propriété, et le fournisseur de banque de messages peut renvoyer le nom de compte et le cachet du compte souhaité.</span><span class="sxs-lookup"><span data-stu-id="4359e-126">Outlook can then call the [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="4359e-127">Pour prendre en charge ces propriétés nommées, les fournisseurs de magasins doivent s’attendre à ce qu’Outlook utilise **IMAPIProp::GetIDsFromNames** pour obtenir la balise de propriété pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4359e-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="4359e-128">Outlook spécifie les valeurs suivantes pour la structure [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) qui correspond à cette propriété nommée, qui est transmise dans le cadre du tableau pointé par le paramètre d’entrée  *lppPropNames*  de **IMAPIProp::GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="4359e-128">Outlook specifies the following values for the [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4359e-129">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="4359e-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="4359e-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4359e-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4359e-131">ulKind :</span><span class="sxs-lookup"><span data-stu-id="4359e-131">ulKind:</span></span>  <br/> |<span data-ttu-id="4359e-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="4359e-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="4359e-133">Kind.lID :</span><span class="sxs-lookup"><span data-stu-id="4359e-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="4359e-134">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="4359e-134">dispidInetAcctStamp</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4359e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4359e-135">See also</span></span>

- [<span data-ttu-id="4359e-136">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="4359e-136">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="4359e-137">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="4359e-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="4359e-138">Propriété canonique PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="4359e-138">PidLidInternetAccountStamp Canonical Property</span></span>](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

