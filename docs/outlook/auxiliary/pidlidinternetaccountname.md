---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Renvoie le nom complet du compte remis le message.
ms.openlocfilehash: 223bc5bbd485426676376d94875274613ff59685
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782808"
---
# <a name="pidlidinternetaccountname"></a><span data-ttu-id="a9cb6-103">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="a9cb6-103">PidLidInternetAccountName</span></span>

<span data-ttu-id="a9cb6-104">Renvoie le nom complet du compte remis le message.</span><span class="sxs-lookup"><span data-stu-id="a9cb6-104">Returns the display name of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a9cb6-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a9cb6-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9cb6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a9cb6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9cb6-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="a9cb6-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="a9cb6-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="a9cb6-108">Property set:</span></span>  <br/> |<span data-ttu-id="a9cb6-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a9cb6-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a9cb6-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="a9cb6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a9cb6-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="a9cb6-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="a9cb6-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a9cb6-112">Data type:</span></span>  <br/> |<span data-ttu-id="a9cb6-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a9cb6-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a9cb6-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="a9cb6-114">Area:</span></span>  <br/> |<span data-ttu-id="a9cb6-115">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="a9cb6-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9cb6-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a9cb6-116">Remarks</span></span>

<span data-ttu-id="a9cb6-117">Cette propriété doit contenir la même valeur que celle qui est renvoyée par la propriété API de gestion de compte [PROP_ACCT_NAME](prop_acct_name.md) pour le compte remis le message.</span><span class="sxs-lookup"><span data-stu-id="a9cb6-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_NAME](prop_acct_name.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="a9cb6-118">Fournisseurs de banque de messages exposent cette propriété nommée et les [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) afin que les actions suivantes se produisent :</span><span class="sxs-lookup"><span data-stu-id="a9cb6-118">Message store providers expose this named property and [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="a9cb6-119">Lorsqu’un utilisateur clique sur **répondre à tous** dans un message électronique, Outlook supprime l’adresse de messagerie qui est associée au compte et est marqué sur le message à partir de la liste des destinataires de la réponse.</span><span class="sxs-lookup"><span data-stu-id="a9cb6-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="a9cb6-120">Ce problème se produit, sauf si cette adresse de messagerie est l’expéditeur du message d’origine.</span><span class="sxs-lookup"><span data-stu-id="a9cb6-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="a9cb6-121">Par défaut, Outlook envoie les réponses et les transferts par le biais du compte qui est marqué sur le message d’origine.</span><span class="sxs-lookup"><span data-stu-id="a9cb6-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="a9cb6-122">En règle générale, le Gestionnaire de protocole Outlook remet des messages et Outlook définit les propriétés **PidLidInternetAccountName** et **PidLidInternetAccountStamp** pour indiquer le compte qui remis le message.</span><span class="sxs-lookup"><span data-stu-id="a9cb6-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="a9cb6-123">Toutefois, si une banque de messages fortement couplée à un type de transport, le Gestionnaire de protocole Outlook ne fournit pas les messages et Outlook ne peut pas définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a9cb6-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="a9cb6-124">Dans ce scénario, Outlook appelle la fonction [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a9cb6-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="a9cb6-125">Si le fournisseur de banque de messages souhaite exposer ces propriétés nommées, il doit implémenter **IMAPIProp::GetIDsFromNames** et renvoyer les balises de propriété via le paramètre de sortie *lppPropTags* .</span><span class="sxs-lookup"><span data-stu-id="a9cb6-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="a9cb6-126">Outlook peut puis appelez la méthode [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) à l’aide de ces balises de propriété, et le fournisseur de banque de message peut renvoyer le nom de compte et le cachet du compte désiré.</span><span class="sxs-lookup"><span data-stu-id="a9cb6-126">Outlook can then call the [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="a9cb6-127">Pour prendre en charge ces propriétés nommées, les fournisseurs de magasins doivent attends qu’Outlook **IMAPIProp::GetIDsFromNames** permet d’obtenir la balise de propriété pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="a9cb6-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="a9cb6-128">Outlook spécifie les valeurs suivantes pour la structure [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) qui correspond à cette propriété nommée, qui est passée en tant que partie de la batterie sur laquelle pointée le paramètre d’entrée *lppPropNames* de **IMAPIProp::GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="a9cb6-128">Outlook specifies the following values for the [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9cb6-129">lpGuid :</span><span class="sxs-lookup"><span data-stu-id="a9cb6-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="a9cb6-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a9cb6-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a9cb6-131">ulKind :</span><span class="sxs-lookup"><span data-stu-id="a9cb6-131">ulKind:</span></span>  <br/> |<span data-ttu-id="a9cb6-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="a9cb6-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="a9cb6-133">Kind.lID :</span><span class="sxs-lookup"><span data-stu-id="a9cb6-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="a9cb6-134">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="a9cb6-134">dispidInetAcctName</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9cb6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9cb6-135">See also</span></span>

- [<span data-ttu-id="a9cb6-136">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="a9cb6-136">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="a9cb6-137">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="a9cb6-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="a9cb6-138">Propriété canonique PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="a9cb6-138">PidLidInternetAccountName Canonical Property</span></span>](http://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

