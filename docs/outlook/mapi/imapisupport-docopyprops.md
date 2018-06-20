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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c93e01b1e4621cddc4c98d528e5f5339cba21dae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783978"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**S’applique à**: Outlook 
  
Copie ou déplace une ou plusieurs propriétés d’un objet à un autre objet.
  
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet avec les propriétés à déplacer ou copier.
    
 _lpSrcObj_
  
> [in] Pointeur vers l’objet qui contient les propriétés pour déplacer ou copier.
    
 _lpIncludeProps_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau compté de balises de propriétés qui indiquent les propriétés pour copier ou déplacer. Le paramètre _lpIncludeProps_ ne peut pas être NULL. 
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent de l’indicateur de progression.
    
 _lpProgress_
  
> [in] Pointeur vers une implémentation d’un indicateur de progression. Si NULL est indiqué dans le paramètre _lpProgress_ , l’indicateur de progression est affichée à l’aide de l’implémentation de MAPI. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpDestInterface_
  
> [in] Pointeur vers l’identificateur d’interface qui représente l’interface à utiliser pour accéder à l’objet pour recevoir les propriétés qui sont copiées ou déplacées.
    
 _lpDestObj_
  
> [in] Pointeur vers l’objet à recevoir les propriétés copiées ou déplacées.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’opération de copie ou de déplacement est effectuée. Les indicateurs suivants peuvent être définis :
    
MAPI_DIALOG 
  
> Affiche un indicateur de progression.
    
MAPI_MOVE 
  
> **DoCopyProps** doit effectuer une opération de déplacement au lieu d’une opération de copie. Lorsque cet indicateur n’est pas défini, **DoCopyProps** effectue une opération de copie. 
    
MAPI_NOREPLACE 
  
> Propriétés existantes dans l’objet de destination ne doivent pas être remplacées. Lorsque cet indicateur n’est pas défini, **DoCopyProps** remplace les propriétés existantes. 
    
 _lppProblems_
  
> [entrée, sortie] À l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; dans le cas contraire, NULL, qui n’indique aucun besoin d’informations sur l’erreur. Si _lppProblems_ est un pointeur valid en entrée, **DoCopyProps** renvoie des informations détaillées sur les erreurs lors de la copie d’une ou plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les propriétés ont été correctement copiées ou déplacées.
    
MAPI_E_COLLISION 
  
> Une propriété à copier ou déplacer déjà existe dans l’objet de destination et l’indicateur MAPI_NOREPLACE est défini. 
    
MAPI_E_FOLDER_CYCLE 
  
> L’objet source, directement ou indirectement contient l’objet de destination. Travail significatifs peut-être avoir été effectué avant cette condition a été détectée, et les objets source et de destination peuvent être modifiées partiellement. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L’interface identifié par le paramètre _lpSrcInterface_ n’est pas pris en charge par l’objet source, ou l’interface identifié par le paramètre _lpDestInterface_ n’est pas pris en charge par l’objet de destination. 
    
MAPI_E_NO_ACCESS 
  
> Une tentative a été effectuée pour accéder à un objet pour lequel l’appelant dispose d’autorisations insuffisantes. Cette erreur est renvoyée si l’objet de destination est identique à l’objet source.
    
Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas en tant que valeurs de retour pour **DoCopyProps**. Ces erreurs s’appliquent à une propriété unique.
  
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et **DoCopyProps** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **DoCopyProps** prend en charge Unicode uniquement. 
    
MAPI_E_COMPUTED 
  
> La propriété ne peut pas être modifiée par l’appelant car il s’agit d’une propriété en lecture seule, calculée par le propriétaire de l’objet de destination. Cette erreur n’est pas lourde ; l’appelant doit autoriser l’opération de copie continuer.
    
MAPI_E_INVALID_TYPE 
  
> Le type de propriété n’est pas valide.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Le type de propriété n’est pas le type attendu par l’appelant.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::DoCopyProps** est implémentée pour les objets de prise en charge de fournisseur de magasin de message. Fournisseurs de banque de messages peuvent appeler **DoCopyProps** pour implémenter la méthode [IMAPIProp::CopyProps](imapiprop-copyprops.md) pour leurs dossiers et des messages. **DoCopyProps** copie ou déplace les propriétés identifiées dans le tableau de balise de propriété désigné par _lpIncludeProps_ et qui sont présentes dans l’objet vers lequel pointé _lpSrcObj_. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Lorsque vous copiez des propriétés entre les objets du même type, tels que les deux messages, les paramètres _lpSrcInterface_ et _lpDestInterface_ doivent contenir les mêmes paramètres interface identificateur et _lpSrcObj_ et _lpDestObj_ doit pointer sur les objets du même type. Si _lpDestInterface_ est défini sur NULL, **DoCopyProps** renvoie MAPI_E_INVALID_PARAMETER. Si vous définissez _lpDestInterface_ à un identificateur d’interface acceptable, mais un ensemble _lpDestObj_ à un pointeur non valide, le résultat est imprévisible. Votre fournisseur échouera probablement. 
  
Définir l’indicateur MAPI_NOREPLACE si vous ne souhaitez pas que les propriétés de l’objet cible pour être remplacé. Propriétés de l’objet cible qui existent dans l’objet source et ne sont pas remplacées ne sont pas supprimées ou modifiées.
  
Pour copier la liste des destinataires d’un message, inclure la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans le tableau de balise de propriété indiqué par le paramètre _lpIncludeProps_ . Pour copier les pièces jointes du message, inclure la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Pour copier un dossier ou hiérarchie du conteneur de carnet d’adresses ou table des matières, inclure **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans le tableau de balise de propriété. Pour inclure la table du contenu associé d’un dossier, inclure la propriété **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) dans le tableau.
  
Si les sous-dossiers sont copiés ou déplacés, leur contenu est copiés ou déplacés dans son intégralité, indépendamment de l’utilisation des propriétés indiqués par la structure **SPropTagArray** . 
  
 Les rapports **DoCopyProps** globales erreurs qui se produisent avec l’opération dans sa globalité et les erreurs qui se produisent avec un ou plusieurs des propriétés individuelles. Ces erreurs individuels sont placés dans une structure **SPropProblemArray** . Vous pouvez supprimer le rapport d’erreurs au niveau de la propriété en passant NULL, plutôt qu’un pointeur valid, pour le paramètre property problème tableau structure. 
  
Si vous souhaitez recevoir des informations sur les erreurs, passez un pointeur de structure **SPropProblemArray** valid dans le paramètre _lppProblems_ . Lorsque **DoCopyProps** renvoie S_OK, vérifiez les erreurs possibles avec des propriétés individuelles dans la structure. Lorsque **DoCopyProps** renvoie une erreur, aucune information n’est retournée dans la structure **SPropProblemArray** . Au lieu de cela, appelez la méthode [IMAPISupport::GetLastError](imapisupport-getlasterror.md) pour récupérer des informations d’erreur détaillé. 
  
Si **DoCopyProps** renvoie S_OK, libérer la structure **SPropProblemArray** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
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

