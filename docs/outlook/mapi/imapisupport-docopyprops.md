---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c5a2de3e74e17e6d6d2250c148a9a865ada9d0db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596084"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace une ou plusieurs propriétés d’un objet vers un autre objet.
  
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet avec les propriétés à copier ou déplacer.
    
 _lpSrcObj_
  
> [in] Pointeur vers l’objet qui contient les propriétés à copier ou déplacer.
    
 _lpIncludeProps_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau compté de balises de propriété qui indiquent les propriétés à copier ou déplacer. Le  _paramètre lpIncludeProps ne_ peut pas être NULL. 
    
 _ulUIParam_
  
> [in] Handle vers la fenêtre parent de l’indicateur de progression.
    
 _lpProgress_
  
> [in] Pointeur vers une implémentation d’un indicateur de progression. Si NULL est transmis dans le  _paramètre lpProgress,_ l’indicateur de progression s’affiche à l’aide de l’implémentation MAPI. Le _paramètre lpProgress est_ ignoré, sauf si l’MAPI_DIALOG est définie dans le paramètre _ulFlags._ 
    
 _lpDestInterface_
  
> [in] Pointeur vers l’identificateur d’interface qui représente l’interface à utiliser pour accéder à l’objet afin de recevoir les propriétés qui sont copiées ou déplacées.
    
 _lpDestObj_
  
> [in] Pointeur vers l’objet pour recevoir les propriétés copiées ou déplacées.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement. Les indicateurs suivants peuvent être définies :
    
MAPI_DIALOG 
  
> Affiche un indicateur de progression.
    
MAPI_MOVE 
  
> **DoCopyProps** doit effectuer une opération de déplacement au lieu d’une opération de copie. Lorsque cet indicateur n’est pas définie, **DoCopyProps** effectue une opération de copie. 
    
MAPI_NOREPLACE 
  
> Les propriétés existantes dans l’objet de destination ne doivent pas être écrasées. Lorsque cet indicateur n’est pas définie, **DoCopyProps** se place sur les propriétés existantes. 
    
 _lppProblems_
  
> [in, out] Lors de l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; dans le cas contraire, NULL, qui indique qu’il n’est pas nécessaire d’obtenir des informations sur l’erreur. Si  _lppProblems est_ un pointeur valide sur l’entrée, **DoCopyProps** renvoie des informations détaillées sur les erreurs de copie d’une ou de plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été correctement copiées ou déplacées.
    
MAPI_E_COLLISION 
  
> Une propriété à copier ou à déplacer existe déjà dans l’objet de destination et l’MAPI_NOREPLACE est définie. 
    
MAPI_E_FOLDER_CYCLE 
  
> L’objet source contient directement ou indirectement l’objet de destination. Des travaux importants ont peut-être été effectués avant la découverte de cette condition, de sorte que les objets source et de destination peuvent être partiellement modifiés. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L’interface identifiée par le paramètre  _lpSrcInterface_ n’est pas prise en charge par l’objet source ou l’interface identifiée par le paramètre  _lpDestInterface_ n’est pas prise en charge par l’objet de destination. 
    
MAPI_E_NO_ACCESS 
  
> Une tentative d’accès à un objet pour lequel l’appelant ne dispose pas des autorisations suffisantes a été tentée. Cette erreur est renvoyée si l’objet de destination est identique à l’objet source.
    
Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray,** mais pas en tant que valeurs de retour **pour DoCopyProps**. Ces erreurs s’appliquent à une seule propriété.
  
MAPI_E_BAD_CHARWIDTH 
  
> L’MAPI_UNICODE a été définie et **DoCopyProps** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **DoCopyProps** prend uniquement en charge Unicode. 
    
MAPI_E_COMPUTED 
  
> La propriété ne peut pas être modifiée par l’appelant, car il s’agit d’une propriété en lecture seule, calculée par le propriétaire de l’objet de destination. Cette erreur n’est pas grave ; L’appelant doit autoriser la continuer l’opération de copie.
    
MAPI_E_INVALID_TYPE 
  
> Le type de propriété n’est pas valide.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Le type de propriété n’est pas celui que l’appelant attend.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::D oCopyProps** est implémentée pour les objets de prise en charge du fournisseur de magasins de messages. Les fournisseurs de magasins de messages peuvent appeler **DoCopyProps** pour implémenter la méthode [IMAPIProp::CopyProps](imapiprop-copyprops.md) pour leurs dossiers et messages. **DoCopyProps** copie ou déplace les propriétés identifiées dans le tableau de balises de propriétés pointées par  _lpIncludeProps_ et qui sont présentes dans l’objet pointé par  _lpSrcObj_. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque vous copiez des propriétés entre des objets du même type, tels que deux messages, les paramètres  _lpSrcInterface_ et  _lpDestInterface_ doivent contenir le même identificateur d’interface, et les paramètres  _lpSrcObj_ et  _lpDestObj_ doivent pointer vers des objets du même type. Si  _lpDestInterface est_ définie sur NULL, **DoCopyProps** renvoie MAPI_E_INVALID_PARAMETER. Si vous définissez  _lpDestInterface_ sur un identificateur d’interface acceptable, mais que vous définissez  _lpDestObj_ sur un pointeur non valide, les résultats sont imprévisibles. Il est fort probable que votre fournisseur échoue. 
  
Définissez l MAPI_NOREPLACE si vous ne souhaitez pas que les propriétés de l’objet de destination soient écrasées. Les propriétés de l’objet de destination qui existent dans l’objet source et qui ne sont pas écrasées ne sont ni supprimées ni modifiées.
  
Pour copier la liste des destinataires d’un message, **incluez** la propriété PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans le tableau de balises de propriétés pointant vers le paramètre _lpIncludeProps._ Pour copier les pièces jointes du message, incluez la **propriété PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Pour copier la hiérarchie ou la table des matières d’un conteneur de dossier ou de carnet d’adresses, incluez **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans le tableau de balises de propriétés. Pour inclure la table des matières associée d’un dossier, incluez la propriété **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) dans le tableau.
  
Si des sous-foldeurs sont copiés ou déplacés, leur contenu est copié ou déplacé dans leur intégralité, quelle que soit l’utilisation des propriétés indiquées par la structure **SPropTagArray.** 
  
 **DoCopyProps signale** les erreurs globales qui se produisent avec l’opération dans son ensemble et les erreurs individuelles qui se produisent avec une ou plusieurs des propriétés. Ces erreurs individuelles sont mises dans une structure **SPropProblemArray.** Vous pouvez supprimer le rapport d’erreurs au niveau de la propriété en passant NULL, plutôt qu’un pointeur valide, pour le paramètre de structure de tableau de problème de propriété. 
  
Si vous souhaitez recevoir des informations sur les erreurs, passez un pointeur de structure **SPropProblemArray** valide dans le paramètre _lppProblems._ Lorsque **DoCopyProps renvoie** S_OK, recherchez les erreurs possibles avec des propriétés individuelles dans la structure. Lorsque **DoCopyProps renvoie** une erreur, aucune information n’est renvoyée dans la structure **SPropProblemArray.** Appelez plutôt la [méthode IMAPISupport::GetLastError](imapisupport-getlasterror.md) pour récupérer des informations détaillées sur l’erreur. 
  
Si **DoCopyProps renvoie** S_OK, libérez la structure **SPropProblemArray** renvoyée en appelant la [fonction MAPIFreeBuffer.](mapifreebuffer.md) 
  
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

