---
title: IMAPIPropCopyProps
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPIPropCopyProps, qui copie ou déplace les propriétés sélectionnées.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
ms.openlocfilehash: dd7bfa9825e30602a0eec863f5b029ba4386c5ab
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816821"
---
# <a name="imapipropcopyprops"></a>IMAPIProp::CopyProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace les propriétés sélectionnées. 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Paramètres

 _lpIncludeProps_
  
> [in] Pointeur vers un tableau de balises de propriétés qui spécifie les propriétés à copier ou à déplacer. **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ne peut pas être inclus dans le tableau. Le paramètre  _lpIncludeProps_ ne peut pas être **null**.
    
 _ulUIParam_
  
> [in] Handle de la fenêtre parente de l’indicateur de progression. 
    
 _lpProgress_
  
> [in] Pointeur vers une implémentation d’un indicateur de progression. Si **null** est passé dans le paramètre _lpProgress_ , l’indicateur de progression s’affiche à l’aide de l’implémentation MAPI. Le paramètre  _lpProgress_ est ignoré, sauf si l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet pointé par le paramètre  _lpDestObj_ . Le paramètre  _lpInterface_ ne doit pas être **null**.
    
 _lpDestObj_
  
> [in] Pointeur vers l’objet pour recevoir les propriétés copiées ou déplacées.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis :
    
MAPI_DECLINE_OK 
  
> Si **CopyProps** appelle la méthode [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) pour gérer l’opération de copie ou de déplacement, elle doit retourner immédiatement avec la valeur d’erreur MAPI_E_DECLINE_COPY. L’indicateur MAPI_DECLINE_OK est défini par MAPI pour limiter la récursivité. Les clients ne définissent pas cet indicateur. 
    
MAPI_DIALOG 
  
> Affiche un indicateur de progression.
    
MAPI_MOVE 
  
> **CopyProps** doit effectuer une opération de déplacement au lieu d’une opération de copie. Lorsque cet indicateur n’est pas défini, **CopyProps** effectue une opération de copie. 
    
MAPI_NOREPLACE 
  
> Les propriétés existantes dans l’objet de destination ne doivent pas être remplacées. Lorsque cet indicateur n’est pas défini, **CopyProps** remplace les propriétés existantes. 
    
 _lppProblems_
  
> [in, out] Lors de l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; sinon, **null**, indiquant qu’il n’est pas nécessaire d’obtenir des informations sur l’erreur. Si  _lppProblems_ est un pointeur valide sur l’entrée, **CopyProps** retourne des informations détaillées sur les erreurs de copie d’une ou plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été correctement copiées ou déplacées.
    
MAPI_E_COLLISION 
  
> Impossible de copier un sous-objet, car un sous-objet portant le même nom d’affichage, défini par la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), existe déjà dans l’objet de destination. 
    
MAPI_E_DECLINE_COPY 
  
> Le fournisseur de services n’implémente pas l’opération de copie.
    
MAPI_E_FOLDER_CYCLE 
  
> L’objet source effectuant l’opération de copie ou de déplacement contient directement ou indirectement l’objet de destination. Un travail important peut avoir été effectué avant la découverte de cette condition, de sorte que les objets source et de destination peuvent être partiellement modifiés. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L’interface identifiée par le paramètre  _lpInterface_ n’est pas prise en charge par l’objet de destination. 
    
MAPI_E_NO_ACCESS 
  
> Une tentative d’accès à un objet pour lequel l’appelant dispose d’autorisations insuffisantes a été effectuée. Cette erreur est retournée si l’objet de destination est identique à l’objet source.
    
Les valeurs suivantes peuvent être retournées dans la structure **SPropProblemArray** , mais pas en tant que valeurs de retour pour **CopyProps**. Ces erreurs s’appliquent à une seule propriété.
  
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été défini et **CopyProps** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et **CopyProps** prend uniquement en charge Unicode. 
    
MAPI_E_COMPUTED 
  
> La propriété ne peut pas être modifiée par l’appelant, car il s’agit d’une propriété en lecture seule, calculée par le propriétaire de l’objet de destination. Cette erreur n’est pas grave; l’appelant doit autoriser la poursuite de l’opération de copie.
    
MAPI_E_INVALID_TYPE 
  
> Le type de propriété n’est pas valide.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Le type de propriété n’est pas le type attendu par l’appelant.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::CopyProps** copie ou déplace les propriétés sélectionnées de l’objet actuel vers un objet de destination. **CopyProps** est principalement utilisé pour répondre aux messages et les transférer, où seules certaines des propriétés du message d’origine voyagent avec la copie de réponse ou de transfert. 
  
Tous les sous-objets de l’objet source sont automatiquement inclus dans l’opération et copiés ou déplacés dans leur intégralité, indépendamment de l’utilisation des propriétés indiquées par la structure [SPropTagArray](sproptagarray.md) . Par défaut, **CopyProps** remplace toutes les propriétés de l’objet de destination qui correspondent aux propriétés de l’objet source. Si l’une des propriétés copiées ou déplacées existe déjà dans l’objet de destination, les propriétés existantes sont remplacées par les nouvelles propriétés, sauf si l’indicateur MAPI_NOREPLACE est défini dans le paramètre _ulFlags_ . Les informations existantes dans l’objet de destination qui ne sont pas remplacées restent intactes. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez fournir une implémentation complète de **CopyProps** ou vous appuyer sur l’implémentation fournie par MAPI dans son objet de support. Si vous souhaitez utiliser l’implémentation MAPI, appelez la méthode **IMAPISupport::D oCopyProps** . Toutefois, si vous déléguez le traitement à **DoCopyProps** et que vous avez passé l’indicateur MAPI_DECLINE_OK, évitez l’appel de support et retournez MAPI_E_DECLINE_COPY à la place. Vous serez appelé avec cet indicateur par MAPI pour éviter la récursivité possible qui peut se produire lorsque vous copiez des dossiers. 
  
Étant donné que l’opération de copie peut être longue, vous devez afficher un indicateur de progression. Utilisez l’implémentation [IMAPIProgress](imapiprogressiunknown.md) qui est passée dans le paramètre _lpProgress_ , le cas échéant. Si  _lpProgress_ a la valeur **Null**, appelez la méthode [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) pour utiliser l’implémentation MAPI. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Ne définissez pas l’indicateur de MAPI_DECLINE_OK ; il est utilisé par MAPI dans ses appels aux implémentations **copyProps** du fournisseur de magasin de messages. 
  
Étant donné que les opérations de copie et de déplacement peuvent prendre du temps, il est judicieux de demander l’affichage d’un indicateur de progression en définissant l’indicateur MAPI_DIALOG. Vous pouvez définir le paramètre  _lpProgress_ sur votre implémentation **d’IMAPIProgress**, si vous en avez un, ou sur **null**. Si  _lpProgress_ est **null**, **CopyProps** utilise l’indicateur de progression par défaut fourni par MAPI. 
  
Vous pouvez supprimer l’affichage d’un indicateur de progression en ne définissant pas l’indicateur MAPI_DIALOG. **CopyProps** ignore les paramètres  _ulUIParam_ et  _lpProgress_ et évite d’afficher l’indicateur. 
  
 **CopyProps** peut signaler des erreurs globales et individuelles, ou des erreurs qui se produisent avec une ou plusieurs des propriétés. Ces erreurs individuelles sont placées dans une structure **SPropProblemArray** . Vous pouvez supprimer la création de rapports d’erreurs au niveau de la propriété en passant **la valeur Null**, au lieu d’un pointeur valide, pour le paramètre de structure du tableau de problèmes de propriétés. 
  
Si vous souhaitez recevoir des informations sur les erreurs, transmettez un pointeur de structure **SPropProblemArray** valide dans le paramètre _lppProblems_ . Lorsque **CopyProps** retourne S_OK, recherchez les erreurs possibles avec des propriétés individuelles dans la structure. Lorsque **CopyProps** retourne une erreur, aucune information n’est retournée dans la structure **SPropProblemArray** . Appelez plutôt la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) pour récupérer des informations détaillées sur les erreurs. 
  
Si **CopyProps** retourne S_OK, libérez la structure **SPropProblemArray** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si vous copiez des propriétés uniques au type d’objet source, vous devez vous assurer que l’objet de destination est du même type. **CopyProps** ne vous empêche pas d’associer des propriétés qui appartiennent généralement à un type d’objet à un autre type d’objet. C’est à vous de copier les propriétés qui ont un sens pour l’objet de destination. Par exemple, vous ne devez pas copier les propriétés de message dans un conteneur de carnet d’adresses. 
  
Pour vous assurer que vous copiez entre des objets du même type, vérifiez que l’objet source et l’objet de destination sont du même type, soit en comparant des pointeurs d’objet, soit en appelant la méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) . Définissez l’identificateur d’interface pointé par  _lpInterface_ sur l’interface standard pour l’objet source. Vérifiez également que le type d’objet ou la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) est identique pour les deux objets. Par exemple, si vous copiez à partir d’un message, définissez  _lpInterface_ sur IID_IMessage et le **PR_OBJECT_TYPE** des deux objets à MAPI_MESSAGE. 
  
Si un pointeur non valide est passé dans le paramètre _lpDestObj_ , les résultats sont imprévisibles. 
  
Pour copier la liste des destinataires d’un message, appelez la méthode **CopyProps** du message et incluez la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans le tableau de balises de propriétés. Pour copier les pièces jointes du message, incluez la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Pour copier la hiérarchie ou la table de contenu d’un dossier ou d’un carnet d’adresses, incluez les propriétés **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans le tableau de balises de propriétés. Pour inclure la table de contenu associée d’un dossier, incluez la propriété **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) dans le tableau. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI utilise la méthode **IMAPIProp::CopyProps** pour copier des propriétés nommées d’un message à un autre. |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |MFCMAPI utilise la méthode **IMAPIProp::CopyProps** pour coller une propriété qui a été copiée à partir d’un autre objet. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propriété canonique PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propriété canonique PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propriété canonique PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)
  
[Propriété canonique PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propriété canonique PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[Propriété canonique PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

