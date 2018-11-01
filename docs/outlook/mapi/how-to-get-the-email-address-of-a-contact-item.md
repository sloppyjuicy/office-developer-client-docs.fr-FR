---
title: Obtention de l’adresse e-mail d’un contact
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: 'Dernière modification : 25 juin 2012'
ms.openlocfilehash: f9c6766c934632a83fa0388ac2bc4c2c397eead6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575552"
---
# <a name="get-the-email-address-of-a-contact-item"></a><span data-ttu-id="fde15-103">Obtention de l’adresse e-mail d’un contact</span><span class="sxs-lookup"><span data-stu-id="fde15-103">Get the email address of a Contact item</span></span>

<span data-ttu-id="fde15-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fde15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fde15-105">Cette rubrique montre comment obtenir la valeur d’une propriété nommée qui représente l’adresse de messagerie d’un élément Microsoft Outlook 2010 ou de contacts Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="fde15-105">This topic shows how to obtain the value of a named property that represents the email address of an Microsoft Outlook 2010 or Microsoft Outlook 2013 Contact item.</span></span>
  
<span data-ttu-id="fde15-106">Vous pouvez associer jusqu'à trois adresses de messagerie avec un élément de Contact dans Outlook 2010 et Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="fde15-106">You can associate up to three email addresses with a Contact item in Outlook 2010 and Outlook 2013.</span></span> <span data-ttu-id="fde15-107">Chaque adresse de messagerie correspond à une propriété de l’objet Outlook 2010 ou Outlook 2013 **ContactItem** dans les modèles objet Outlook 2010 et Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="fde15-107">Each email address corresponds to a property of the Outlook 2010 or Outlook 2013 **ContactItem** object in the Outlook 2010 and Outlook 2013 object models.</span></span> <span data-ttu-id="fde15-108">Interne à Outlook 2010 et Outlook 2013, l’adresse de messagerie correspond à une propriété nommée de MAPI.</span><span class="sxs-lookup"><span data-stu-id="fde15-108">Internal to Outlook 2010 and Outlook 2013, the email address also corresponds to a MAPI named property.</span></span> <span data-ttu-id="fde15-109">Par exemple, la première adresse de messagerie d’un contact correspond à la propriété **Email1Address** de **ContactItem** dans les modèles objet Outlook 2010 et Outlook 2013 et le [nommé interne Outlook 2010 et Outlook 2013 Propriété canonique PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="fde15-109">For example, the first email address of a contact corresponds to the **Email1Address** property of the **ContactItem** in the Outlook 2010 and Outlook 2013 object models, and the Outlook 2010 and Outlook 2013 internal named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).</span></span>
  
<span data-ttu-id="fde15-110">Pour obtenir la valeur d’une adresse de messagerie d’un élément de contact, vous pouvez utiliser l’objet **PropertyAccessor** du modèle objet Outlook 2010 ou Outlook 2013, ou tout d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété de la propriété nommée, puis Spécifiez cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="fde15-110">To obtain the value of an email address of a contact item, you can use the **PropertyAccessor** object of the Outlook 2010 or Outlook 2013 object model, or first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag of the named property, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="fde15-111">Lors de l’appel **IMAPIProp::GetIDsFromNames**, spécifiez les valeurs appropriées pour la structure [MAPINAMEID](mapinameid.md) sur laquelle pointé le paramètre d’entrée _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="fde15-111">When calling **IMAPIProp::GetIDsFromNames**, specify the appropriate values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_.</span></span> <span data-ttu-id="fde15-112">L’exemple de code suivant montre comment obtenir la première adresse de messagerie d’un contact spécifique, `lpContact`, à l’aide de **GetIDsFromNames** et **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="fde15-112">The following code sample shows how to obtain the first email address of a specified contact,  `lpContact`, using **GetIDsFromNames** and **GetProps**.</span></span> 
  
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


