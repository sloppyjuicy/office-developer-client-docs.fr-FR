---
title: Obtention de l’adresse e-mail d’un contact
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: fab09d0c594bac1374973f523abe6ff0b9c09dd0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429592"
---
# <a name="get-the-email-address-of-a-contact-item"></a><span data-ttu-id="eb31e-103">Obtention de l’adresse e-mail d’un contact</span><span class="sxs-lookup"><span data-stu-id="eb31e-103">Get the email address of a Contact item</span></span>

<span data-ttu-id="eb31e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb31e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb31e-105">Cette rubrique montre comment obtenir la valeur d'une propriété nommée qui représente l'adresse de messagerie d'un élément de contact Microsoft Outlook 2010 ou Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="eb31e-105">This topic shows how to obtain the value of a named property that represents the email address of an Microsoft Outlook 2010 or Microsoft Outlook 2013 Contact item.</span></span>
  
<span data-ttu-id="eb31e-106">Vous pouvez associer jusqu'à trois adresses de messagerie à un élément de contact dans Outlook 2010 et Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="eb31e-106">You can associate up to three email addresses with a Contact item in Outlook 2010 and Outlook 2013.</span></span> <span data-ttu-id="eb31e-107">Chaque adresse de messagerie correspond à une propriété de l'objet Outlook 2010 ou Outlook 2013 **ContactItem** dans les modèles d'objet Outlook 2010 et Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="eb31e-107">Each email address corresponds to a property of the Outlook 2010 or Outlook 2013 **ContactItem** object in the Outlook 2010 and Outlook 2013 object models.</span></span> <span data-ttu-id="eb31e-108">En interne à Outlook 2010 et Outlook 2013, l'adresse de messagerie correspond également à une propriété nommée MAPI.</span><span class="sxs-lookup"><span data-stu-id="eb31e-108">Internal to Outlook 2010 and Outlook 2013, the email address also corresponds to a MAPI named property.</span></span> <span data-ttu-id="eb31e-109">Par exemple, la première adresse de messagerie d'un contact correspond à la propriété **Email1Address** de l'objet **ContactItem** dans les modèles d'objets outlook 2010 et Outlook 2013, et le nom interne outlook 2010 et Outlook 2013 nommé [ Propriété canonique PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="eb31e-109">For example, the first email address of a contact corresponds to the **Email1Address** property of the **ContactItem** in the Outlook 2010 and Outlook 2013 object models, and the Outlook 2010 and Outlook 2013 internal named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).</span></span>
  
<span data-ttu-id="eb31e-110">Pour obtenir la valeur d'une adresse de messagerie d'un contact, vous pouvez utiliser l'objet **propertyAccessor** du modèle objet Outlook 2010 ou Outlook 2013, ou utiliser d'abord [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété de la propriété nommée, puis Spécifiez cette balise de propriété dans [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="eb31e-110">To obtain the value of an email address of a contact item, you can use the **PropertyAccessor** object of the Outlook 2010 or Outlook 2013 object model, or first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag of the named property, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="eb31e-111">Lors de l'appel de **IMAPIProp:: GetIDsFromNames**, spécifiez les valeurs appropriées pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d'entrée _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="eb31e-111">When calling **IMAPIProp::GetIDsFromNames**, specify the appropriate values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_.</span></span> <span data-ttu-id="eb31e-112">L'exemple de code suivant montre comment obtenir la première adresse de messagerie d'un contact spécifié `lpContact`, à l'aide de **GetIDsFromNames** et de **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="eb31e-112">The following code sample shows how to obtain the first email address of a specified contact,  `lpContact`, using **GetIDsFromNames** and **GetProps**.</span></span> 
  
```cpp
HRESULT HrGetEmail1(LPMESSAGE lpContact) 
{ 
    HRESULT hRes = S_OK; 
    LPSPropTagArray lpNamedPropTags = NULL; 
    MAPINAMEID NamedID = {0}; 
    LPMAPINAMEID lpNamedID = &NamedID; 
    NamedID.lpguid = (LPGUID)&PSETID_Address; 
    NamedID.ulKind = MNID_ID; 
    NamedID.Kind.lID = dispidEmailEmailAddress; 
 
    hRes = lpContact->GetIDsFromNames( 
           1,  
           &lpNamedID,  
           NULL,  
           &lpNamedPropTags); 
 
    if (SUCCEEDED(hRes) && lpNamedPropTags) 
    { 
        SPropTagArray sPropTagArray; 
 
        sPropTagArray.cValues = 1; 
        sPropTagArray.aulPropTag[0] = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[0],PT_STRING8); 
        LPSPropValue lpProps = NULL; 
        ULONG cProps = 0; 
 
        hRes = lpContact->GetProps( 
               &sPropTagArray, 
               NULL, 
               &cProps, 
               &lpProps); 
        if (SUCCEEDED(hRes) &&  
            1 == cProps &&  
            lpProps &&  
            PT_STRING8 == PROP_TYPE(lpProps[0].ulPropTag) && 
            lpProps[0].Value.lpszA) 
        { 
            printf("Email address 1 = \"%s\"\n",lpProps[0].Value.lpszA); 
        } 
        MAPIFreeBuffer(lpProps); 
        MAPIFreeBuffer(lpNamedPropTags); 
     } 
     return hRes; 
}
```


