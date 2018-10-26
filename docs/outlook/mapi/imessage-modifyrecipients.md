---
title: IMessageModifyRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.ModifyRecipients
api_type:
- COM
ms.assetid: 2625f29d-325f-417d-bcec-49d580f9cd7e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0735008575db5e1cab62dbde4b699b15e04cedb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567285"
---
# <a name="imessagemodifyrecipients"></a><span data-ttu-id="c9ee6-103">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="c9ee6-103">IMessage::ModifyRecipients</span></span>

  
  
<span data-ttu-id="c9ee6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9ee6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9ee6-105">Ajoute, supprime ou modifie des destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-105">Adds, deletes, or modifies message recipients.</span></span>
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a><span data-ttu-id="c9ee6-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="c9ee6-106">Parameters</span></span>

 <span data-ttu-id="c9ee6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c9ee6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c9ee6-p101">[in] Masque de bits d'indicateurs qui contr�le les modifications apport�es par destinataire. Si la valeur z�ro est transmise au param�tre  _ulFlags_, **ModifyRecipients** remplace tous les destinataires existantes avec la liste des destinataires d�sign�e par le param�tre  _lpMods_. Les indicateurs suivants peuvent �tre d�finis pour  _ulFlags_:</span><span class="sxs-lookup"><span data-stu-id="c9ee6-p101">[in] Bitmask of flags that controls the recipient changes. If zero is passed for the  _ulFlags_ parameter, **ModifyRecipients** replaces all existing recipients with the recipient list pointed to by the  _lpMods_ parameter. The following flags can be set for  _ulFlags_:</span></span>
    
<span data-ttu-id="c9ee6-111">MODRECIP_ADD</span><span class="sxs-lookup"><span data-stu-id="c9ee6-111">MODRECIP_ADD</span></span> 
  
> <span data-ttu-id="c9ee6-112">Les destinataires d�sign�s par le param�tre  _lpMods_ doivent �tre ajout�es � la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-112">The recipients pointed to by the  _lpMods_ parameter should be added to the recipient list.</span></span> 
    
<span data-ttu-id="c9ee6-113">MODRECIP_MODIFY</span><span class="sxs-lookup"><span data-stu-id="c9ee6-113">MODRECIP_MODIFY</span></span> 
  
> <span data-ttu-id="c9ee6-p102">Les destinataires d�sign�s par le param�tre  _lpMods_ doivent remplacer les destinataires existants. Toutes les propri�t�s existantes sont remplac�es par celles de la structure [ADRENTRY](adrentry.md) correspondante.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-p102">The recipients pointed to by the  _lpMods_ parameter should replace existing recipients. All of the existing properties are replaced by those in the corresponding [ADRENTRY](adrentry.md) structure.</span></span> 
    
<span data-ttu-id="c9ee6-116">MODRECIP_REMOVE</span><span class="sxs-lookup"><span data-stu-id="c9ee6-116">MODRECIP_REMOVE</span></span> 
  
> <span data-ttu-id="c9ee6-117">Destinataires existants doivent être retirés de la liste des destinataires à l’aide sous forme d’index de la propriété **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) incluse dans le tableau de valeurs de propriété de chaque entrée du destinataire dans le paramètre _lpMods_ .</span><span class="sxs-lookup"><span data-stu-id="c9ee6-117">Existing recipients should be removed from the recipient list using as an index the **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) property included in the property value array of each recipient entry in the  _lpMods_ parameter.</span></span> 
    
 <span data-ttu-id="c9ee6-118">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="c9ee6-118">_lpMods_</span></span>
  
> <span data-ttu-id="c9ee6-119">[in] Pointeur vers une structure [ADRLIST](adrlist.md) qui contient une liste de destinataires pour �tre ajout�s, supprim�s ou modifi�s dans le message.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-119">[in] Pointer to an [ADRLIST](adrlist.md) structure that contains a list of recipients to be added, deleted, or modified in the message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c9ee6-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c9ee6-120">Return value</span></span>

<span data-ttu-id="c9ee6-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9ee6-121">S_OK</span></span> 
  
> <span data-ttu-id="c9ee6-122">La liste des destinataires a �t� modifi�e avec succ�s.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-122">The recipient list was successfully modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9ee6-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="c9ee6-123">Remarks</span></span>

<span data-ttu-id="c9ee6-p103">La m�thode **IMessage::ModifyRecipients** modifie la liste des destinataires du message. Il est � partir de cette liste, organis�e dans une structure [ADRLIST](adrlist.md) , que la table de destinataires est g�n�r�e.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-p103">The **IMessage::ModifyRecipients** method changes the message's recipient list. It is from this list, held in an [ADRLIST](adrlist.md) structure, that the recipient table is built.</span></span> 
  
<span data-ttu-id="c9ee6-126">La structure **ADRLIST** contient une structure [ADRENTRY](adrentry.md) pour chaque destinataire et chaque structure **ADRENTRY** contient un tableau de valeurs de propri�t�s d�crivant les propri�t�s du destinataire.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-126">The **ADRLIST** structure contains one [ADRENTRY](adrentry.md) structure for each recipient and each **ADRENTRY** structure contains an array of property values describing the recipient properties.</span></span> 
  
<span data-ttu-id="c9ee6-127">Destinataires de la structure **ADRLIST** peuvent �tre r�solus ou non r�solues.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-127">Recipients in the **ADRLIST** structure can be resolved or unresolved.</span></span> <span data-ttu-id="c9ee6-128">La diff�rence r�side dans le nombre et le type des propri�t�s qui sont inclus.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-128">The difference is in the number and type of properties that are included.</span></span> <span data-ttu-id="c9ee6-129">Un destinataire non résolu contienne uniquement les **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et les propriétés de **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) pendant un destinataire résolu contient ces deux propriétés ainsi que \*\*TYPEADR_PR \*\*([PidTagAddressType](pidtagaddresstype-canonical-property.md)) et **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c9ee6-129">An unresolved recipient contains only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) properties while a resolved recipient contains those two properties plus **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span> <span data-ttu-id="c9ee6-130">Si **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) est disponible, il peut être inclus également.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-130">If **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is available, it can be included also.</span></span>
  
<span data-ttu-id="c9ee6-p105">Au moment o� qu'un message est envoy�, il doit inclure uniquement les destinataires r�solus dans sa liste des destinataires. Destinataires non r�solus provoquent des rapports de non-remise � �tre cr�� et envoy� � l'exp�diteur d'origine du message. Pour plus d'informations sur le processus de r�solution de nom � partir du point de vue du client, consultez la rubrique [r�solution d'un nom](resolving-a-recipient-name.md). Pour plus d'informations � partir du point de vue du fournisseur de carnet d'adresses, voir [Impl�mentation de la r�solution de noms](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="c9ee6-p105">By the time a message is submitted, it must include only resolved recipients in its recipient list. Unresolved recipients cause nondelivery reports to be created and sent to the original sender of the message. For more information about the name resolution process from the client perspective, see [Resolving a Name](resolving-a-recipient-name.md). For more information from the perspective of the address book provider, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="c9ee6-p106">En plus des destinataires r�solus et non r�solus, un destinataire peut �tre NULL. Le membre **cValues** de la structure **ADRENTRY** pour le destinataire est d�fini sur z�ro et le membre **rgPropVals** est d�fini sur NULL.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-p106">In addition to resolved and unresolved recipients, a recipient can be NULL. The **cValues** member of the **ADRENTRY** structure for the recipient is set to zero and the **rgPropVals** member is set to NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c9ee6-137">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="c9ee6-137">Notes to callers</span></span>

<span data-ttu-id="c9ee6-p107">Vous pouvez cr�er une liste de destinataires en appelant [IAddrBook::Address](imapisupport-address.md) pour afficher la bo�te de dialogue commune et demandez � l'utilisateur de s�lectionner des entr�es. La liste d'adresses d�sign�e par le param�tre  _lppAdrList_ pour **Address** peut �tre transmise aux **ModifyRecipients** en tant que param�tre  _lpMods_.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-p107">You can create a recipient list by calling [IAddrBook::Address](imapisupport-address.md) to display the common dialog box and prompt the user to select entries. The address list pointed to by the  _lppAdrList_ parameter to **Address** can be passed to **ModifyRecipients** as the  _lpMods_ parameter.</span></span> 
  
<span data-ttu-id="c9ee6-p108">Lorsque vous sp�cifiez les propri�t�s d'un destinataire dans la structure [ADRLIST](adrlist.md) , inclure toutes les propri�t�s du destinataire, non seulement celles nouvelles ou modifi�es. Lorsqu'un destinataire est modifi�, toutes les propri�t�s non incluses dans la structure **ADRLIST** sont supprim�es. Pour r�cup�rer l'ensemble actuel des propri�t�s pour tous les destinataires d'un message, appelez [GetRecipientTable](imessage-getrecipienttable.md) et r�cup�rer toutes les lignes. Un **SRowSet** �tant identique en structure � une **ADRLIST**, vous pouvez les utiliser indiff�remment.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-p108">When you specify properties for a recipient in the [ADRLIST](adrlist.md) structure, include all of the recipient's properties, not only the new or changed ones. When a recipient is modified, any properties not included in the **ADRLIST** structure are deleted. To retrieve the current set of properties for all of a message's recipients, call [GetRecipientTable](imessage-getrecipienttable.md) and retrieve all of the rows. Because an **SRowSet** is identical in structure to an **ADRLIST**, you can use them interchangeably.</span></span>
  
 <span data-ttu-id="c9ee6-144">**ModifyRecipients** remplace toutes les entr�es dans la liste des destinataires en cours avec les informations d�sign�es par  _lpMods_ lorsque aucun des indicateurs sont d�finies dans le param�tre  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-144">**ModifyRecipients** replaces all of the entries in the current recipient list with the information pointed to by  _lpMods_ when none of the flags are set in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c9ee6-145">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="c9ee6-145">Notes to callers</span></span>

<span data-ttu-id="c9ee6-p109">Lorsque vous d�finissez l'indicateur MODRECIP_MODIFY, **ModifyRecipients** remplace chaque destinataire toute ligne par la ligne associ�e dans la structure [ADRLIST](adrlist.md) transmise dans  _lpMods_. Veillez � sp�cifier toutes les propri�t�s ayant un destinataire doit qu'elles ont chang� pour emp�cher leur involontairement supprim�.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-p109">When you set the MODRECIP_MODIFY flag, **ModifyRecipients** replaces each entire recipient row with the associated row in the [ADRLIST](adrlist.md) structure passed in  _lpMods_. Be careful to specify all of the properties that a recipient should have regardless of whether they have changed to prevent them from being unintentionally deleted.</span></span>
  
<span data-ttu-id="c9ee6-148">Voici quelques r�gles pour d�finir les propri�t�s des destinataires dans la structure **ADRLIST**:</span><span class="sxs-lookup"><span data-stu-id="c9ee6-148">Following are some rules for setting the properties of the recipients in the **ADRLIST** structure:</span></span> 
  
- <span data-ttu-id="c9ee6-p110">N'utilisez pas PT_NULL comme un type de propri�t�. **ModifyRecipients** renvoie une erreur si vous rencontrez cette valeur.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-p110">Do not use PT_NULL as a property type. **ModifyRecipients** returns an error when encountering this value.</span></span> 
    
- <span data-ttu-id="c9ee6-p111">N'utilisez pas PT_ERROR comme un type de propri�t�. **ModifyRecipients** ignore cette valeur.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-p111">Do not use PT_ERROR as a property type. **ModifyRecipients** ignores this value.</span></span> 
    
- <span data-ttu-id="c9ee6-153">Inclure la propri�t� **PR_ROWID** pour tous les destinataires lorsque vous d�finissez l'indicateur MODRECIP_MODIFY ou MODRECIP_REMOVE dans  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-153">Include the **PR_ROWID** property for all recipients when you set either the MODRECIP_REMOVE or MODRECIP_MODIFY flag in  _ulFlags_.</span></span> 
    
- <span data-ttu-id="c9ee6-154">N'incluez pas de la propri�t� **PR_ROWID** pour tous les destinataires lorsque vous d�finissez l'indicateur MODRECIP_ADD dans  _ulFlags_ ou lorsque vous transf�rez la valeur z�ro dans  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-154">Do not include the **PR_ROWID** property for any of the recipients when you set the MODRECIP_ADD flag in  _ulFlags_ or when you pass zero in  _ulFlags_.</span></span>
    
<span data-ttu-id="c9ee6-p112">Si vous incluez soit la **PR_ADDRTYPE** propri�t� ou **PR_EMAIL_ADDRESS** pour un destinataire et un ou deux de ces propri�t�s sont incompatibles avec le type d'adresse et l'adresse du destinataire comme identifi� par **PR_ENTRYID**, les r�sultats ne sont pas d�finis. En d'autres termes, il existe trois possibilit�s, selon le fournisseur de services :</span><span class="sxs-lookup"><span data-stu-id="c9ee6-p112">If you include either the **PR_ADDRTYPE** property or **PR_EMAIL_ADDRESS** property for a recipient and one or both of these properties are inconsistent with the address type and address of the recipient as identified by **PR_ENTRYID**, the results are undefined. That is, there are three possibilities, depending on the service provider:</span></span>
  
- <span data-ttu-id="c9ee6-157">Le message est remis � l'adresse d�crit par les propri�t�s **PR_ADDRTYPE** et **PR_EMAIL_ADDRESS**.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-157">The message will be delivered to the address described by the **PR_ADDRTYPE** and **PR_EMAIL_ADDRESS** properties.</span></span> 
    
- <span data-ttu-id="c9ee6-158">Le message est remis au destinataire identifi� par **PR_ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-158">The message will be delivered to the recipient identified by **PR_ENTRYID**.</span></span>
    
- <span data-ttu-id="c9ee6-159">Le message sera d�clar� non remis en raison de l'ambigu�t� de l'adresse.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-159">The message will be declared undeliverable due to the ambiguity of the address information.</span></span>
    
<span data-ttu-id="c9ee6-p113">Utiliser les r�gles de r�partition d�crites dans la [Gestion de la m�moire ADRLIST et SRowSet des Structures](managing-memory-for-adrlist-and-srowset-structures.md) d'allocation de m�moire pour la liste des destinataires. **ModifyRecipients** ne la lib�re pas la structure **ADRLIST** ni aucun de ses sous-structures. La structure **ADRLIST** et chaque [SPropValue](spropvalue.md) doivent �tre allou�s s�par�ment � l'aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) telle que chacun peut �tre lib�r� individuellement. Si la m�thode requiert un espace suppl�mentaire pour n'importe quelle structure **SPropValue**, elle peut remplacer la structure de **SPropValue** avec un fichier qui peut ult�rieurement lib�r� � l'aide de [MAPIFreeBuffer](mapifreebuffer.md). La structure **SPropValue** d'origine doit aussi �tre lib�r�e � l'aide de **MAPIFreeBuffer**.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-p113">Use the allocation rules outlined in [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md) to allocate memory for the recipient list. **ModifyRecipients** does not free the **ADRLIST** structure nor any of its substructures. The **ADRLIST** structure and each [SPropValue](spropvalue.md) structure must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function such that each can be freed individually. If the method requires additional space for any **SPropValue** structure, it can replace the **SPropValue** structure with a new one that can later be freed using [MAPIFreeBuffer](mapifreebuffer.md). The original **SPropValue** structure should also be freed using **MAPIFreeBuffer**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c9ee6-165">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c9ee6-165">MFCMAPI reference</span></span>

<span data-ttu-id="c9ee6-166">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-166">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c9ee6-167">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="c9ee6-167">**File**</span></span>|<span data-ttu-id="c9ee6-168">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="c9ee6-168">**Function**</span></span>|<span data-ttu-id="c9ee6-169">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c9ee6-169">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9ee6-170">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="c9ee6-170">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c9ee6-171">Ajouter destinataire</span><span class="sxs-lookup"><span data-stu-id="c9ee6-171">AddRecipient</span></span>  <br/> |<span data-ttu-id="c9ee6-172">MFCMAPI utilise la m�thode **IMessage::ModifyRecipients** pour ajouter un destinataire � un message.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-172">MFCMAPI uses the **IMessage::ModifyRecipients** method to add a new recipient to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9ee6-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9ee6-173">See also</span></span>



[<span data-ttu-id="c9ee6-174">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="c9ee6-174">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="c9ee6-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="c9ee6-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="c9ee6-176">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="c9ee6-176">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="c9ee6-177">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="c9ee6-177">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="c9ee6-178">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c9ee6-178">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="c9ee6-179">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c9ee6-179">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c9ee6-180">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c9ee6-180">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="c9ee6-181">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c9ee6-181">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="c9ee6-182">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="c9ee6-182">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

