---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5569e52a5e4865e6e343da38ba60fa6fef2e087c
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62461854"
---
# <a name="imapisupportdocopyto"></a>IMAPISupport::DoCopyTo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace toutes les propriétés d’un objet, à l’exception des propriétés spécifiquement exclues, vers un autre objet.
  
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet qui possède les propriétés à copier ou à déplacer.
    
 _lpSrcObj_
  
> [in] Pointeur vers l’objet qui possède les propriétés à copier ou déplacer.
    
 _ciidExclude_
  
> [in] Nombre d’interfaces à exclure lorsque vous copiez ou déplacez des propriétés.
    
 _eaidExclude_
  
> [in] Tableau d’identificateurs d’interface qui indique les interfaces qui ne doivent pas être utilisées lorsque vous copiez ou déplacez des informations supplémentaires vers l’objet de destination.
    
 _lpExcludeProps_
  
> [in] Pointeur vers un tableau de balises de propriétés qui identifie les balises de propriété qui doivent être exclues de l’opération de copie ou de déplacement. La transmission de null dans _le paramètre lpExcludeProps_ indique que toutes les propriétés de l’objet doivent être copiées ou déplacées. **DoCopyTo** renvoie MAPI_E_INVALID_PARAMETER lorsque le membre **cValues** de la structure [SPropTagArray](sproptagarray.md) pointée par  _lpExcludeProps_ est définie sur 0. 
    
 _ulUIParam_
  
> [in] Handle vers la fenêtre parent de l’indicateur de progression. 
    
 _lpProgress_
  
> [in] Pointeur vers une implémentation d’indicateur de progression. Si NULL est transmis dans _le paramètre lpProgress_ , MAPI fournit l’implémentation de progression. Le  _paramètre lpProgress est_ ignoré, sauf si l’MAPI_DIALOG est définie dans _le paramètre ulFlags_ . 
    
 _lpDestInterface_
  
> [in] Pointeur vers l’identificateur d’interface qui représente l’interface à utiliser pour accéder à l’objet afin de recevoir les propriétés copiées ou déplacées.
    
 _lpDestObj_
  
> [in] Pointeur vers l’objet pour recevoir les propriétés copiées ou déplacées.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement. Les indicateurs suivants peuvent être définies :
    
MAPI_DIALOG 
  
> Affiche un indicateur de progression. 
    
MAPI_MOVE 
  
> **DoCopyTo doit** effectuer une opération de déplacement au lieu d’une opération de copie. Lorsque cet indicateur n’est pas définie, **DoCopyTo** effectue une opération de copie. 
    
MAPI_NOREPLACE 
  
> Les propriétés existantes dans l’objet de destination ne doivent pas être écrasées. Lorsque cet indicateur n’est pas définie, **DoCopyTo** se place sur les propriétés existantes. 
    
 _lppProblems_
  
> [out] Lors de l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; dans le cas contraire, NULL, qui indique qu’il n’est pas nécessaire d’obtenir des informations sur l’erreur. Si  _lppProblems est_ un pointeur valide sur l’entrée, **DoCopyTo** renvoie des informations détaillées sur les erreurs de copie d’une ou plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été correctement copiées ou déplacées.
    
MAPI_E_COLLISION 
  
> Une propriété à copier ou à déplacer existe déjà dans l’objet de destination et l’MAPI_NOREPLACE est définie. 
    
MAPI_E_FOLDER_CYCLE 
  
> L’objet source contient directement ou indirectement l’objet de destination. Des travaux importants ont peut-être été effectués avant la découverte de cette condition, de sorte que les objets source et de destination peuvent être partiellement modifiés. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L’interface identifiée par le paramètre  _lpSrcInterface_ n’est pas prise en charge par l’objet pointé par  _lpSrcObj_, ou l’interface identifiée par le paramètre  _lpDestInterface_ n’est pas prise en charge par l’objet pointé par  _lpDestObj_. 
    
MAPI_E_NO_ACCESS 
  
> Une tentative d’accès à un objet pour lequel l’appelant dispose d’autorisations insuffisantes a été tentée. Cette erreur est renvoyée si l’objet de destination est identique à l’objet source.
    
MAPI_E_INVALID_PARAMETER 
  
> Le  _paramètre lpSrcInterface est_ NULL. 
    
Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas en tant que valeurs de retour **pour DoCopyTo**. Ces erreurs s’appliquent à une seule propriété.
  
MAPI_E_BAD_CHARWIDTH 
  
> L’MAPI_UNICODE a été définie et **DoCopyTo** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **DoCopyTo** prend uniquement en charge Unicode. 
    
MAPI_E_COMPUTED 
  
> La propriété ne peut pas être modifiée par l’appelant, car il s’agit d’une propriété en lecture seule, calculée par le propriétaire de l’objet de destination. Cette erreur n’est pas grave ; L’appelant doit autoriser la continuer l’opération de copie.
    
MAPI_E_INVALID_TYPE 
  
> Le type de propriété n’est pas valide.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Le type de propriété n’est pas le type attendu par l’appelant.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::D oCopyTo** est implémentée pour les objets de prise en charge du fournisseur de magasins de messages. Les fournisseurs de magasins de messages peuvent appeler **DoCopyTo** pour implémenter la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) pour leurs dossiers et messages. 
  
Par défaut, **DoCopyTo** copie ou déplace toutes les propriétés d’un objet vers un autre objet. Tous les sous-objets de l’objet source sont automatiquement inclus dans l’opération et copiés ou déplacés dans leur intégralité. 
  
Si l’une des propriétés copiées ou déplacées existe déjà dans l’objet de destination, les propriétés existantes sont écrasées par les nouvelles propriétés, sauf si l’indicateur MAPI_NOREPLACE est définie dans le paramètre _ulFlags_ . Les informations existantes dans l’objet de destination qui ne sont pas écrasées restent intactes. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour exclure des propriétés de l’opération de copie ou de déplacement, incluez leurs balises de propriété dans le paramètre _lpExcludeProps_ . Si vous passez les résultats de l’utilisation de la macro [PROP_TAG](prop_tag.md) pour créer une balise de propriété à partir d’un identificateur spécifique dans le tableau de balises de propriétés, toutes les propriétés avec cet identificateur seront exclues. Par exemple, l’entrée suivante dans le tableau de balises de propriétés exclut toutes les propriétés dont l’identificateur est 0x8002, quel que soit le type : 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Pour éviter de copier l’heure de remise d’un message lorsque vous copiez le message dans un autre dossier, spécifiez **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) dans le tableau d’exclusion de balise de propriété. Pour exclure la liste des destinataires d’un message, ajoutez la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) au tableau d’exclusion. Pour exclure les pièces jointes d’un message, ajoutez la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) au tableau.
  
De même, pour empêcher la copie ou le déplacement de la hiérarchie ou de la table des matières d’un conteneur de dossiers ou de carnets d’adresses, incluez **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans le tableau d’exclusion de balise de propriété.
  
Ignorez MAPI_E_COMPUTED erreurs renvoyées dans la structure **SPropProblemArray** dans _le paramètre lppProblems_ . 
  
L’identificateur d’interface vers qui  _pointe lpSrcInterface_ est généralement identique à l’identificateur d’interface vers qui  _pointe lpDestInterface_ . 
  
Si vous passez un identificateur d’interface acceptable dans  _lpDestInterface_ mais un pointeur non valide dans  _lpDestObj_, les résultats sont imprévisibles. Il est très probable que cela entraîne l’échec de votre fournisseur. 
  
À l’inverse, si vous avez connaissance d’informations supplémentaires qui ne doivent pas être copiées ou déplacées, ajoutez les identificateurs d’interface pour les interfaces à exclure dans le tableau transmis dans le paramètre _converseidExclude_ . Par exemple, si vous copiez des messages, mais pas leurs pièces jointes, passez les IID_IMessage dans le tableau _eaidExclude_ . **DoCopyTo** ignore les interfaces répertoriées dans  _rgidExclude_ qu’il ne reconnaît pas. 
  
Lorsque vous utilisez le  _paramètre autantidExclude_ que pour exclure une interface, il exclut également toutes les interfaces dérivées de cette interface. Par exemple, l’exclusion de l’interface [IMAPIContainer](imapicontainerimapiprop.md) entraîne l’exclusion des dossiers ou des conteneurs de carnet d’adresses, selon le type de fournisseur. N’excluez [pas IMAPIProp](imapipropiunknown.md) ou [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) , car de nombreuses interfaces en dérivent. 
  
 **DoCopyTo signale les** erreurs globales qui s’appliquent à l’opération dans son ensemble et les erreurs individuelles qui s’appliquent à des propriétés individuelles. Ces erreurs individuelles sont mises dans une structure **SPropProblemArray** . Vous pouvez supprimer le rapport d’erreurs au niveau de la propriété en passant NULL, plutôt qu’un pointeur valide, pour le paramètre de structure de tableau de problème de propriété. 
  
Si vous souhaitez recevoir des informations sur les erreurs, passez un pointeur de structure **SPropProblemArray** valide dans le paramètre _lppProblems_ . Lorsque **DoCopyTo renvoie** S_OK, recherchez les erreurs possibles avec des propriétés individuelles dans la structure. Lorsque **DoCopyTo renvoie** une erreur, aucune information n’est renvoyée dans la structure **SPropProblemArray** . Appelez plutôt la [méthode IMAPISupport::GetLastError](imapisupport-getlasterror.md) pour récupérer des informations détaillées sur l’erreur. 
  
Si **DoCopyTo renvoie** S_OK, libérez la structure **SPropProblemArray** renvoyée en appelant la [fonction MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si une erreur globale se produit lors de l’appel **DoCopyTo** , n’utilisez pas ou ne llibérez pas la structure **SPropProblemArray** . Les fournisseurs doivent ignorer le  _membre ulIndex_ dans **les structures SPropProblemArray** renvoyées par **DoCopyTo**.
  
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

