---
title: Implémentation d’un objet de contrôle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b4b225f7e048ef40a79c4b258629cb01b79368d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565829"
---
# <a name="control-object-implementation"></a><span data-ttu-id="feb93-103">Implémentation d’un objet de contrôle</span><span class="sxs-lookup"><span data-stu-id="feb93-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="feb93-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="feb93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="feb93-105">Contrôler les objets ou les objets qui prennent en charge la [IMAPIControl : IUnknown](imapicontroliunknown.md) de l’interface, sont implémentés par les fournisseurs pour ajouter une fonctionnalité à un bouton qui s’affiche dans une boîte de dialogue MAPI.</span><span class="sxs-lookup"><span data-stu-id="feb93-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="feb93-106">Objets de contrôle peuvent être implémentés uniquement pour les boutons.</span><span class="sxs-lookup"><span data-stu-id="feb93-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="feb93-107">**IMAPIControl** a trois méthodes : [GetLastError](imapicontrol-getlasterror.md) [GetState](imapicontrol-getstate.md)et [Activer](imapicontrol-activate.md).</span><span class="sxs-lookup"><span data-stu-id="feb93-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="feb93-108">**GetState** pour déterminer s’il faut désactiver le bouton appels MAPI.</span><span class="sxs-lookup"><span data-stu-id="feb93-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="feb93-109">**GetState** est appelée dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="feb93-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="feb93-110">Lorsque la boîte de dialogue dans laquelle s’affiche le bouton premier affichage.</span><span class="sxs-lookup"><span data-stu-id="feb93-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="feb93-111">Lorsqu’une notification de la table affichage est émise pour le bouton.</span><span class="sxs-lookup"><span data-stu-id="feb93-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="feb93-112">Définir le contenu du paramètre _lpulState_ pour MAPI_DISABLED si l’utilisateur ne peut pas interagir avec le bouton MAPI_ENABLED si l’utilisateur peut interagir.</span><span class="sxs-lookup"><span data-stu-id="feb93-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="feb93-113">Lorsque l’utilisateur clique sur le bouton, **Activer**appels MAPI.</span><span class="sxs-lookup"><span data-stu-id="feb93-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="feb93-114">**Activer** effectue la tâche qui a été associée avec le bouton.</span><span class="sxs-lookup"><span data-stu-id="feb93-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="feb93-115">Cette tâche peut être tout ce qui convient pour votre fournisseur, telles qu’affichant une boîte de dialogue ou la mise à jour d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="feb93-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="feb93-116">Si la tâche échoue parce que l’utilisateur a annulé, renvoyer MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="feb93-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="feb93-117">Pour d’autres causes d’échec, renvoie la valeur d’erreur appropriés.</span><span class="sxs-lookup"><span data-stu-id="feb93-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="feb93-118">Si la tâche se déroule correctement, et elle est liée à un changement de propriété qui apparaissent dans un autre contrôle dans la boîte de dialogue, appelez [ITableData::HrNotify](itabledata-hrnotify.md).</span><span class="sxs-lookup"><span data-stu-id="feb93-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="feb93-119">**HrNotify** est appelé pour émettre une notification de table complet avec la propriété **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) de la propriété modifiée dans la structure [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="feb93-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="feb93-120">Ne placez pas la nouvelle valeur de propriété dans la structure ; au lieu de cela, elle retourne lorsque [IMAPIProp::GetProps](imapiprop-getprops.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="feb93-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="feb93-121">Généralement, une notification de la table affichage ne peut être utilisée pour désactiver ou activer un contrôle, il peut être utilisé avec un bouton.</span><span class="sxs-lookup"><span data-stu-id="feb93-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="feb93-122">MAPI actualise le contrôle modifié pour répondre à la notification.</span><span class="sxs-lookup"><span data-stu-id="feb93-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="feb93-123">MAPI appelle la méthode du contrôle **GetLastError** lorsque **Activate** renvoie une erreur autre que MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="feb93-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="feb93-124">Si **GetLastError** place les informations d’erreur étendue dans la structure [MAPIERROR](mapierror.md) qu’elle renvoie le contenu du paramètre _lppMAPIError_ , MAPI affiche pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="feb93-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="feb93-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="feb93-125">See also</span></span>



[<span data-ttu-id="feb93-126">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="feb93-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

