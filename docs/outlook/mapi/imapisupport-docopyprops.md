---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322364"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace une ou plusieurs propriétés d'un objet vers un autre objet.
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
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
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à l'objet avec les propriétés à copier ou déplacer.
    
 _lpSrcObj_
  
> dans Pointeur vers l'objet qui contient les propriétés à copier ou déplacer.
    
 _lpIncludeProps_
  
> dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau compté de balises de propriété qui indiquent les propriétés à copier ou déplacer. Le paramètre _lpIncludeProps_ ne peut pas être null. 
    
 _ulUIParam_
  
> dans Handle de la fenêtre parent de l'indicateur de progression.
    
 _lpProgress_
  
> dans Pointeur vers une implémentation d'un indicateur de progression. Si la valeur NULL est transmise au paramètre _lpProgress_ , l'indicateur de progression est affiché à l'aide de l'implémentation MAPI. Le paramètre _lpProgress_ est ignoré sauf si l'indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpDestInterface_
  
> dans Pointeur vers l'identificateur d'interface qui représente l'interface à utiliser pour accéder à l'objet afin de recevoir les propriétés qui sont copiées ou déplacées.
    
 _lpDestObj_
  
> dans Pointeur vers l'objet pour recevoir les propriétés copiées ou déplacées.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'exécution de l'opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis:
    
MAPI_DIALOG 
  
> Affiche un indicateur de progression.
    
MAPI_MOVE 
  
> **DoCopyProps** doit effectuer une opération de déplacement au lieu d'une opération de copie. Lorsque cet indicateur n'est pas défini, **DoCopyProps** effectue une opération de copie. 
    
MAPI_NOREPLACE 
  
> Les propriétés existantes dans l'objet de destination ne doivent pas être remplacées. Lorsque cet indicateur n'est pas défini, **DoCopyProps** remplace les propriétés existantes. 
    
 _lppProblems_
  
> [in, out] Lors de l'entrée, pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; Sinon, NULL, ce qui indique qu'il n'est pas nécessaire d'obtenir des informations sur l'erreur. Si _lppProblems_ est un pointeur valide sur l'entrée, **DoCopyProps** renvoie des informations détaillées sur les erreurs lors de la copie d'une ou de plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été correctement copiées ou déplacées.
    
MAPI_E_COLLISION 
  
> Une propriété à copier ou à déplacer existe déjà dans l'objet de destination et l'indicateur MAPI_NOREPLACE est défini. 
    
MAPI_E_FOLDER_CYCLE 
  
> L'objet source contient directement ou indirectement l'objet de destination. Un travail significatif a pu être effectué avant la découverte de cette condition, de sorte que les objets source et de destination puissent être partiellement modifiés. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L'interface identifiée par le paramètre _lpSrcInterface_ n'est pas prise en charge par l'objet source, ou l'interface identifiée par le paramètre _lpDestInterface_ n'est pas prise en charge par l'objet de destination. 
    
MAPI_E_NO_ACCESS 
  
> Une tentative d'accès à un objet pour lequel l'appelant ne dispose pas des autorisations suffisantes a été effectuée. Cette erreur est renvoyée si l'objet de destination est identique à l'objet source.
    
Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas comme valeurs de retour pour **DoCopyProps**. Ces erreurs s'appliquent à une seule propriété.
  
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et **DoCopyProps** ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et **DoCopyProps** prend en charge uniquement Unicode. 
    
MAPI_E_COMPUTED 
  
> La propriété ne peut pas être modifiée par l'appelant car il s'agit d'une propriété en lecture seule, calculée par le propriétaire de l'objet de destination. Cette erreur n'est pas grave; l'appelant doit autoriser la poursuite de l'opération de copie.
    
MAPI_E_INVALID_TYPE 
  
> Le type de propriété n'est pas valide.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Le type de propriété n'est pas le type attendu par l'appelant.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::D ocopyprops** est implémentée pour les objets de prise en charge du fournisseur de banque de messages. Les fournisseurs de banques de messages peuvent appeler **DoCopyProps** pour implémenter la méthode [IMAPIProp:: CopyProps](imapiprop-copyprops.md) pour leurs dossiers et messages. **DoCopyProps** copie ou déplace les propriétés qui sont identifiées dans le tableau de balises de propriété pointé par _lpIncludeProps_ et présentes dans l'objet pointé par _lpSrcObj_. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque vous copiez des propriétés entre des objets du même type, comme deux messages, les paramètres _lpSrcInterface_ et _lpDestInterface_ doivent contenir le même identificateur d'interface, ainsi que les paramètres _lpSrcObj_ et _lpDestObj_ doit pointer vers des objets du même type. Si _lpDestInterface_ est défini sur null, **DoCopyProps** renvoie MAPI_E_INVALID_PARAMETER. Si vous définissez _lpDestInterface_ sur un identificateur d'interface acceptable, mais que vous définissez _lpDestObj_ sur un pointeur non valide, les résultats sont imprévisibles. Il est probable que votre fournisseur échoue. 
  
Définissez l'indicateur MAPI_NOREPLACE si vous ne souhaitez pas que les propriétés de l'objet de destination soient remplacées. Les propriétés de l'objet de destination qui existent dans l'objet source et qui ne sont pas remplacées ne sont pas supprimées ni modifiées.
  
Pour copier la liste des destinataires d'un message, incluez la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans le tableau des balises de propriété pointé par le paramètre _lpIncludeProps_ . Pour copier les pièces jointes du message, incluez la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Pour copier la table de hiérarchie ou de contenu d'un conteneur de carnet d'adresses ou de dossier, incluez **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans le tableau de balises de propriété. Pour inclure le tableau de contenu associé à un dossier, incluez la propriété **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) dans le tableau.
  
Si des sous-dossiers sont copiés ou déplacés, leur contenu est copié ou déplacé dans leur intégralité, indépendamment de l'utilisation des propriétés indiquées par la structure **SPropTagArray** . 
  
 **DoCopyProps** signale les erreurs globales qui se produisent avec l'opération dans son ensemble, ainsi que les erreurs individuelles qui se produisent avec une ou plusieurs des propriétés. Ces erreurs individuelles sont placées dans une structure **SPropProblemArray** . Vous pouvez supprimer le rapport d'erreurs au niveau de la propriété en passant NULL, plutôt qu'un pointeur valide, pour le paramètre de structure de tableau de problèmes de propriété. 
  
Si vous souhaitez recevoir des informations sur les erreurs, transmettez un pointeur de structure **SPropProblemArray** valide dans le paramètre _lppProblems_ . Lorsque **DoCopyProps** renvoie S_OK, vérifiez la possibilité d'éventuelles erreurs avec des propriétés individuelles dans la structure. Lorsque **DoCopyProps** renvoie une erreur, aucune information n'est renvoyée dans la structure **SPropProblemArray** . À la place, appelez la méthode [IMAPISupport:: GetLastError](imapisupport-getlasterror.md) pour extraire des informations détaillées sur les erreurs. 
  
Si **DoCopyProps** renvoie S_OK, libérez la structure **SPropProblemArray** renvoyée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::CopyProps](imapiprop-copyprops.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[Propriété canonique PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propriété canonique PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propriété canonique PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)
  
[Propriété canonique PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propriété canonique PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

