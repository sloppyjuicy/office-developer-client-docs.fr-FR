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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331807"
---
# <a name="imapisupportdocopyto"></a>IMAPISupport::DoCopyTo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace toutes les propriétés d'un objet, à l'exception des propriétés spécifiquement exclues, vers un autre objet.
  
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
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à l'objet dont les propriétés doivent être copiées ou déplacées.
    
 _lpSrcObj_
  
> dans Pointeur vers l'objet dont les propriétés doivent être copiées ou déplacées.
    
 _ciidExclude_
  
> dans Nombre d'interfaces à exclure lorsque vous copiez ou déplacez des propriétés.
    
 _rgiidExclude_
  
> dans Tableau d'identificateurs d'interface qui indique les interfaces qui ne doivent pas être utilisées lorsque vous copiez ou déplacez des informations supplémentaires vers l'objet de destination.
    
 _lpExcludeProps_
  
> dans Pointeur vers un tableau de balises de propriété qui identifie les balises de propriété qui doivent être exclues de l'opération de copie ou de déplacement. Le fait de transmettre NULL dans le paramètre _lpExcludeProps_ indique que toutes les propriétés de l'objet doivent être copiées ou déplacées. **DoCopyTo** renvoie MAPI_E_INVALID_PARAMETER lorsque le membre **cValues** de la structure [SPropTagArray](sproptagarray.md) vers laquelle pointe _lpExcludeProps_ est défini sur 0. 
    
 _ulUIParam_
  
> dans Handle de la fenêtre parent de l'indicateur de progression. 
    
 _lpProgress_
  
> dans Pointeur vers une implémentation d'indicateur de progression. Si NULL est transmis dans le paramètre _lpProgress_ , MAPI fournit l'implémentation de la progression. Le paramètre _lpProgress_ est ignoré sauf si l'indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpDestInterface_
  
> dans Pointeur vers l'identificateur d'interface qui représente l'interface à utiliser pour accéder à l'objet afin de recevoir les propriétés copiées ou déplacées.
    
 _lpDestObj_
  
> dans Pointeur vers l'objet pour recevoir les propriétés copiées ou déplacées.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle l'opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis:
    
MAPI_DIALOG 
  
> Affiche un indicateur de progression. 
    
MAPI_MOVE 
  
> **DoCopyTo** doit effectuer une opération de déplacement au lieu d'une opération de copie. Lorsque cet indicateur n'est pas défini, **DoCopyTo** effectue une opération de copie. 
    
MAPI_NOREPLACE 
  
> Les propriétés existantes dans l'objet de destination ne doivent pas être remplacées. Lorsque cet indicateur n'est pas défini, **DoCopyTo** remplace les propriétés existantes. 
    
 _lppProblems_
  
> remarquer Lors de l'entrée, pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; Sinon, NULL, ce qui indique qu'il n'est pas nécessaire d'obtenir des informations sur l'erreur. Si _lppProblems_ est un pointeur valide sur l'entrée, **DoCopyTo** renvoie des informations détaillées sur les erreurs lors de la copie d'une ou de plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été correctement copiées ou déplacées.
    
MAPI_E_COLLISION 
  
> Une propriété à copier ou à déplacer existe déjà dans l'objet de destination et l'indicateur MAPI_NOREPLACE est défini. 
    
MAPI_E_FOLDER_CYCLE 
  
> L'objet source contient directement ou indirectement l'objet de destination. Un travail significatif a pu être effectué avant la découverte de cette condition, de sorte que les objets source et de destination puissent être partiellement modifiés. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L'interface identifiée par le paramètre _lpSrcInterface_ n'est pas prise en charge par l'objet désigné par _lpSrcObj_, ou l'interface identifiée par le paramètre _lpDestInterface_ n'est pas prise en charge par l'objet désigné par _lpDestObj _. 
    
MAPI_E_NO_ACCESS 
  
> Une tentative d'accès à un objet pour lequel l'appelant ne dispose pas des autorisations suffisantes a été effectuée. Cette erreur est renvoyée si l'objet de destination est identique à l'objet source.
    
MAPI_E_INVALID_PARAMETER 
  
> Le paramètre _lpSrcInterface_ est null. 
    
Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas comme valeurs de retour pour **DoCopyTo**. Ces erreurs s'appliquent à une seule propriété.
  
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et **DoCopyTo** ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et **DoCopyTo** prend en charge uniquement Unicode. 
    
MAPI_E_COMPUTED 
  
> La propriété ne peut pas être modifiée par l'appelant car il s'agit d'une propriété en lecture seule, calculée par le propriétaire de l'objet de destination. Cette erreur n'est pas grave; l'appelant doit autoriser la poursuite de l'opération de copie.
    
MAPI_E_INVALID_TYPE 
  
> Le type de propriété n'est pas valide.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Le type de propriété n'est pas le type attendu par l'appelant.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::D ocopyto** est implémentée pour les objets de prise en charge du fournisseur de banque de messages. Les fournisseurs de banques de messages peuvent appeler **DoCopyTo** pour implémenter la méthode [IMAPIProp:: CopyTo](imapiprop-copyto.md) pour leurs dossiers et messages. 
  
Par défaut, **DoCopyTo** copie ou déplace toutes les propriétés d'un objet vers un autre objet. Tous les sous-objets de l'objet source sont automatiquement inclus dans l'opération et copiés ou déplacés dans leur intégralité. 
  
Si une des propriétés copiées ou déplacées existe déjà dans l'objet de destination, les propriétés existantes sont remplacées par les nouvelles propriétés, sauf si l'indicateur MAPI_NOREPLACE est défini dans le paramètre _ulFlags_ . Les informations existantes de l'objet de destination qui ne sont pas remplacées restent intactes. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour exclure les propriétés de l'opération de copie ou de déplacement, incluez les balises de propriété dans le paramètre _lpExcludeProps_ . Si vous transmettez les résultats de l'utilisation de la macro [PROP_TAG](prop_tag.md) pour créer une balise de propriété à partir d'un identificateur spécifique dans le tableau de balises de propriété, toutes les propriétés dotées de cet identificateur seront exclues. Par exemple, l'entrée suivante dans le tableau de la balise de propriété entraîne l'exclusion de toutes les propriétés dotées d'un identificateur 0x8002, quel que soit le type: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Pour éviter de copier le délai de remise d'un message lorsque vous copiez le message dans un autre dossier, spécifiez **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) dans la balise de propriété Exclude Array. Pour exclure la liste de destinataires d'un message, ajoutez la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) au tableau d'exclusion. Pour exclure les pièces jointes d'un message, ajoutez la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) au tableau.
  
De même, pour empêcher la copie ou le changement de la table de hiérarchie ou de contenu d'un dossier ou d'un conteneur de carnet d'adresses, incluez **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans la balise de propriété Exclude Array.
  
Ignore les erreurs MAPI_E_COMPUTED renvoyées dans la structure **SPropProblemArray** dans le paramètre _lppProblems_ . 
  
L'identificateur d'interface auquel _lpSrcInterface_ pointe est généralement identique à l'identificateur d'interface sur lequel _lpDestInterface_ pointe. 
  
Si vous transmettez un identificateur d'interface acceptable dans _lpDestInterface_ mais un pointeur non valide dans _lpDestObj_, les résultats sont imprévisibles. Cela peut entraîner l'échec de votre fournisseur. 
  
À l'inverse, si vous connaissez des informations supplémentaires qui ne doivent pas être copiées ou déplacées, ajoutez les identificateurs d'interface pour les interfaces à exclure dans le tableau passé dans le paramètre _rgiidExclude_ . Par exemple, si vous copiez des messages, mais pas les pièces jointes de leurs messages, transmettez IID_IMessage dans le tableau _rgiidExclude_ . **DoCopyTo** ignore toutes les interfaces figurant dans _rgiidExclude_ qu'il ne reconnaît pas. 
  
Lorsque vous utilisez le paramètre _rgiidExclude_ pour exclure une interface, il exclut également toutes les interfaces dérivées de cette interface. Par exemple, l'exclusion de l'interface [IMAPIContainer](imapicontainerimapiprop.md) entraîne l'exclusion des dossiers ou des conteneurs du carnet d'adresses, selon le type de fournisseur. N'excluez pas [IMAPIProp](imapipropiunknown.md) ou [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) car un grand nombre d'interfaces dérivent de celles-ci. 
  
 **DoCopyTo** signale les erreurs globales qui s'appliquent à l'opération dans son ensemble, ainsi que les erreurs individuelles qui s'appliquent aux propriétés individuelles. Ces erreurs individuelles sont placées dans une structure **SPropProblemArray** . Vous pouvez supprimer le rapport d'erreurs au niveau de la propriété en passant NULL, plutôt qu'un pointeur valide, pour le paramètre de structure de tableau de problèmes de propriété. 
  
Si vous souhaitez recevoir des informations sur les erreurs, transmettez un pointeur de structure **SPropProblemArray** valide dans le paramètre _lppProblems_ . Lorsque **DoCopyTo** renvoie S_OK, vérifiez la possibilité d'éventuelles erreurs avec des propriétés individuelles dans la structure. Lorsque **DoCopyTo** renvoie une erreur, aucune information n'est renvoyée dans la structure **SPropProblemArray** . À la place, appelez la méthode [IMAPISupport:: GetLastError](imapisupport-getlasterror.md) pour extraire des informations détaillées sur les erreurs. 
  
Si **DoCopyTo** renvoie S_OK, libérez la structure **SPropProblemArray** renvoyée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si une erreur globale se produit lors de l'appel **DoCopyTo** , n'utilisez pas ou ne libérez pas la structure **SPropProblemArray** . Les fournisseurs doivent ignorer le membre _ulIndex_ dans les structures **SPropProblemArray** renvoyées par **DoCopyTo**.
  
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

