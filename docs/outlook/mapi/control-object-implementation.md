---
title: Implémentation d'un objet de contrôle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8304021565638f8a5893d0be8cd6a94ed62a8d95
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422606"
---
# <a name="control-object-implementation"></a><span data-ttu-id="fc59c-103">Implémentation d'un objet de contrôle</span><span class="sxs-lookup"><span data-stu-id="fc59c-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="fc59c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc59c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc59c-105">Les objets Control, ou les objets qui prennent en charge l'interface [IMAPIControl: IUnknown](imapicontroliunknown.md) , sont implémentés par les fournisseurs pour ajouter des fonctionnalités à un bouton qui apparaît dans une boîte de dialogue MAPI.</span><span class="sxs-lookup"><span data-stu-id="fc59c-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="fc59c-106">Les objets Control ne peuvent être implémentés que pour les boutons.</span><span class="sxs-lookup"><span data-stu-id="fc59c-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="fc59c-107">**IMAPIControl** possède trois méthodes: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md)et [activer](imapicontrol-activate.md).</span><span class="sxs-lookup"><span data-stu-id="fc59c-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="fc59c-108">MAPI appelle **GetState** pour déterminer si le bouton doit être désactivé ou non.</span><span class="sxs-lookup"><span data-stu-id="fc59c-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="fc59c-109">**GetState** est appelé dans les situations suivantes:</span><span class="sxs-lookup"><span data-stu-id="fc59c-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="fc59c-110">Lorsque la boîte de dialogue dans laquelle apparaît le bouton s'affiche pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="fc59c-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="fc59c-111">Lorsqu'une notification de table d'affichage est générée pour le bouton.</span><span class="sxs-lookup"><span data-stu-id="fc59c-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="fc59c-112">Définissez le contenu du paramètre _lpulState_ sur MAPI_DISABLED si l'utilisateur ne peut pas interagir avec le bouton et MAPI_ENABLED si l'utilisateur peut interagir.</span><span class="sxs-lookup"><span data-stu-id="fc59c-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="fc59c-113">Lorsque l'utilisateur clique sur le bouton, \*\*\*\* MAPI appelle la méthode Activate.</span><span class="sxs-lookup"><span data-stu-id="fc59c-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="fc59c-114">**Activate** effectue la tâche associée au bouton.</span><span class="sxs-lookup"><span data-stu-id="fc59c-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="fc59c-115">Cette tâche peut être tout à fait appropriée pour votre fournisseur, telle que l'affichage d'une boîte de dialogue ou la mise à jour d'une propriété.</span><span class="sxs-lookup"><span data-stu-id="fc59c-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="fc59c-116">Si la tâche échoue parce que l'utilisateur l'a annulée, retournez MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="fc59c-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="fc59c-117">Pour les autres causes de l'échec, renvoyez la valeur d'erreur appropriée.</span><span class="sxs-lookup"><span data-stu-id="fc59c-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="fc59c-118">Si la tâche réussit et qu'elle est liée à une modification de propriété qui apparaît dans un autre contrôle de la boîte de dialogue, appelez [ITableData:: HrNotify](itabledata-hrnotify.md).</span><span class="sxs-lookup"><span data-stu-id="fc59c-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="fc59c-119">**HrNotify** est appelé pour émettre une notification de table d'affichage avec la propriété **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) de la propriété modifiée dans la structure [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="fc59c-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="fc59c-120">Ne placez pas la nouvelle valeur de la propriété dans la structure; à la place, renvoyez-le lorsque [IMAPIProp:: GetProps](imapiprop-getprops.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="fc59c-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="fc59c-121">Bien qu'une notification de table d'affichage ne puisse pas être utilisée pour désactiver ou activer un contrôle, elle peut être utilisée avec un bouton.</span><span class="sxs-lookup"><span data-stu-id="fc59c-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="fc59c-122">MAPI actualise le contrôle modifié pour répondre à la notification.</span><span class="sxs-lookup"><span data-stu-id="fc59c-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="fc59c-123">MAPI appelle la méthode **GetLastError** du contrôle lorsque \*\*\*\* la méthode Activate renvoie une erreur autre que MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="fc59c-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="fc59c-124">Si **GetLastError** place des informations d'erreur étendues dans la structure [MAPIERROR](mapierror.md) qu'il renvoie dans le contenu du paramètre _lppMAPIError_ , MAPI l'affiche pour l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fc59c-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc59c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc59c-125">See also</span></span>



[<span data-ttu-id="fc59c-126">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="fc59c-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

