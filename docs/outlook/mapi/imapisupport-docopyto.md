---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390631"
---
# <a name="imapisupportdocopyto"></a>IMAPISupport::DoCopyTo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace toutes les propriétés d’un objet, à l’exception des propriétés exclues en particulier, à un autre objet.
  
```cpp
HRESULT DoCopyTo(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  ULONG ciidExclude,
  LPCIID rgiidExclude,
  LPSPropTagArray lpExcludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Paramètres

 _lpSrcInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet qui a les propriétés à déplacer ou copier.
    
 _lpSrcObj_
  
> [in] Pointeur vers l’objet qui a les propriétés à déplacer ou copier.
    
 _ciidExclude_
  
> [in] Le nombre d’interfaces à exclure lorsque vous copiez ou déplacez les propriétés.
    
 _rgiidExclude_
  
> [in] Un tableau d’identificateurs d’interface qui indique les interfaces qui ne doivent pas être utilisés lorsque vous copiez ou déplacez des informations supplémentaires à l’objet de destination.
    
 _lpExcludeProps_
  
> [in] Pointeur vers un tableau de balise de propriété qui identifie les balises de propriété qui doivent être exclus de la copie ou l’opération de déplacement. Passage de NULL dans le paramètre _lpExcludeProps_ indique que toutes les propriétés de l’objet doivent être copiés ou déplacés. **DoCopyTo** renvoie MAPI_E_INVALID_PARAMETER lorsque le membre **cValues** de la structure [SPropTagArray](sproptagarray.md) désignés par _lpExcludeProps_ est définie sur 0. 
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent de l’indicateur de progression. 
    
 _lpProgress_
  
> [in] Pointeur vers une implémentation d’indicateur de progression. Si NULL est indiqué dans le paramètre _lpProgress_ , MAPI fournit l’implémentation de progression. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpDestInterface_
  
> [in] Pointeur vers l’identificateur d’interface qui représente l’interface à utiliser pour accéder à l’objet pour recevoir les propriétés copiées ou déplacées.
    
 _lpDestObj_
  
> [in] Pointeur vers l’objet à recevoir les propriétés copiées ou déplacées.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis :
    
MAPI_DIALOG 
  
> Affiche un indicateur de progression. 
    
MAPI_MOVE 
  
> **DoCopyTo** doit effectuer une opération de déplacement au lieu d’une opération de copie. Lorsque cet indicateur n’est pas défini, **DoCopyTo** effectue une opération de copie. 
    
MAPI_NOREPLACE 
  
> Propriétés existantes dans l’objet de destination ne doivent pas être remplacées. Lorsque cet indicateur n’est pas défini, **DoCopyTo** remplace les propriétés existantes. 
    
 _lppProblems_
  
> [out] À l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; dans le cas contraire, NULL, qui n’indique aucun besoin d’informations sur l’erreur. Si _lppProblems_ est un pointeur valid en entrée, **DoCopyTo** renvoie des informations détaillées sur les erreurs lors de la copie d’une ou plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été copiées ou déplacées.
    
MAPI_E_COLLISION 
  
> Une propriété à copier ou déplacer déjà existe dans l’objet de destination et l’indicateur MAPI_NOREPLACE est défini. 
    
MAPI_E_FOLDER_CYCLE 
  
> L’objet source, directement ou indirectement contient l’objet de destination. Travail significatifs peut-être avoir été effectué avant cette condition a été détectée, et les objets source et de destination peuvent être modifiées partiellement. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L’interface identifié par le paramètre _lpSrcInterface_ n’est pas pris en charge par l’objet vers lequel pointé _lpSrcObj_ou de l’interface identifié par le paramètre _lpDestInterface_ n’est pas pris en charge par l’objet vers lequel pointé _lpDestObj _. 
    
MAPI_E_NO_ACCESS 
  
> Une tentative a été effectuée pour accéder à un objet pour lequel l’appelant dispose d’autorisations insuffisantes. Cette erreur est renvoyée si l’objet de destination est identique à l’objet source.
    
MAPI_E_INVALID_PARAMETER 
  
> Le paramètre _lpSrcInterface_ est NULL. 
    
Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas en tant que valeurs de retour pour **DoCopyTo**. Ces erreurs s’appliquent à une propriété unique.
  
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et **DoCopyTo** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **DoCopyTo** prend en charge Unicode uniquement. 
    
MAPI_E_COMPUTED 
  
> La propriété ne peut pas être modifiée par l’appelant car il s’agit d’une propriété en lecture seule, calculée par le propriétaire de l’objet de destination. Cette erreur n’est pas lourde ; l’appelant doit autoriser l’opération de copie continuer.
    
MAPI_E_INVALID_TYPE 
  
> Le type de propriété n’est pas valide.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Le type de propriété n’est pas le type attendu par l’appelant.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::DoCopyTo** est implémentée pour les objets de prise en charge de fournisseur de magasin de message. Fournisseurs de banque de messages peuvent appeler **DoCopyTo** pour implémenter la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) pour leurs dossiers et des messages. 
  
Par défaut, **DoCopyTo** copie ou déplace toutes les propriétés d’un objet à un autre objet. Les sous-objets de l’objet source sont automatiquement inclus dans l’opération et copiés ou déplacés dans leur intégralité. 
  
Si les propriétés copiées ou déplacées existent déjà dans l’objet de destination, les propriétés existantes sont remplacées par les nouvelles propriétés, sauf si l’indicateur MAPI_NOREPLACE est défini dans le paramètre _ulFlags_ . Les informations existantes dans l’objet de destination n’est pas remplacé sont conservées. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour exclure les propriétés de la copie ou l’opération de déplacement, inclut les balises de propriété dans le paramètre _lpExcludeProps_ . Si vous passez les résultats de l’utilisation de la macro [PROP_TAG](prop_tag.md) pour créer une balise de propriété à partir d’un identificateur spécifique dans le tableau de balise de propriété, toutes les propriétés de cet identificateur seront exclues. Par exemple, l’entrée suivante dans le tableau de la propriété tag, toutes les propriétés d’un identificateur de 0x8002 à exclure, quel que soit le type : 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Pour éviter de copier l’heure de remise d’un message lorsque vous copiez le message vers un autre dossier, spécifiez **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) dans la propriété tag exclure le tableau. Pour exclure la liste des destinataires d’un message, ajoutez la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans le tableau exclure. Pour exclure les pièces jointes d’un message, ajoutez la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) dans le tableau.
  
De même, pour éviter la copie ou le déplacement d’un dossier ou hiérarchie du conteneur de carnet d’adresses ou table des matières, incluez **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans la propriété tag exclure tableau.
  
MAPI_E_COMPUTED ignorer les erreurs renvoyées dans la structure **SPropProblemArray** dans le paramètre _lppProblems_ . 
  
L’identificateur d’interface _lpSrcInterface_ pointe vers est généralement identique à l’identificateur d’interface qui pointe _lpDestInterface_ vers. 
  
Si vous passez un identificateur d’interface acceptable dans _lpDestInterface_ un pointeur non valide dans _lpDestObj_, le résultat est imprévisible. Cela entraîne probablement votre fournisseur d’échec. 
  
Inversement, si vous avez pris connaissance des informations supplémentaires qui ne doivent pas être copiées ou déplacées, ajoutez les identificateurs d’interface pour les interfaces à exclure dans le tableau passé dans le paramètre _rgiidExclude_ . Par exemple, si vous copiez des messages, mais pas les pièces jointes de leurs messages, transmettez IID_IMessage dans le tableau _rgiidExclude_ . **DoCopyTo** ignore toutes les interfaces répertoriées dans _rgiidExclude_ qu’il ne reconnaît pas. 
  
Lorsque vous utilisez le paramètre _rgiidExclude_ pour exclure une interface, il exclut également toutes les interfaces dérivées de cette interface. Par exemple, à l’exception de l’interface [IMAPIContainer](imapicontainerimapiprop.md) , dossiers ou conteneurs de carnet d’adresses à exclure, selon le type de fournisseur. N’excluent pas [IMAPIProp](imapipropiunknown.md) ou [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) , car les interfaces autant dérivent de ces derniers. 
  
 **DoCopyTo** signale les erreurs globaux qui s’appliquent à l’opération dans sa globalité et des erreurs spécifiques qui s’appliquent à des propriétés individuelles. Ces erreurs individuels sont placés dans une structure **SPropProblemArray** . Vous pouvez supprimer le rapport d’erreurs au niveau de la propriété en passant NULL, plutôt qu’un pointeur valid, pour le paramètre property problème tableau structure. 
  
Si vous souhaitez recevoir des informations sur les erreurs, passez un pointeur de structure **SPropProblemArray** valid dans le paramètre _lppProblems_ . Lorsque **DoCopyTo** renvoie S_OK, vérifiez les erreurs possibles avec des propriétés individuelles dans la structure. Lorsque **DoCopyTo** renvoie une erreur, aucune information n’est retournée dans la structure **SPropProblemArray** . Au lieu de cela, appelez la méthode [IMAPISupport::GetLastError](imapisupport-getlasterror.md) pour récupérer des informations d’erreur détaillé. 
  
Si **DoCopyTo** renvoie S_OK, libérer la structure **SPropProblemArray** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si une erreur globale se produit lors de l’appel **DoCopyTo** , ne pas utiliser ou libérer la structure **SPropProblemArray** . Fournisseurs doivent ignorer le membre _ulIndex_ dans des structures **SPropProblemArray** retourné par **DoCopyTo**.
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPISupport::CopyFolder](imapisupport-copyfolder.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[Propriété canonique PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propriété canonique PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propriété canonique PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propriété canonique PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)
  
[Propriété canonique PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

