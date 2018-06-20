---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ff8f13a1dcf678e1d05b6e8e083597156422b83d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783914"
---
# <a name="imapipropcopyprops"></a>IMAPIProp::CopyProps

  
  
**S’applique à**: Outlook 
  
Copie ou déplace des propriétés sélectionnées. 
  
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
  
> [in] Pointeur vers un tableau de balise de propriété qui spécifie les propriétés pour copier ou déplacer. **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ne peut pas être incluse dans le tableau. Le paramètre _lpIncludeProps_ ne peut pas être **null**.
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent de l’indicateur de progression. 
    
 _lpProgress_
  
> [in] Pointeur vers une implémentation d’un indicateur de progression. Si **null** est passé dans le paramètre _lpProgress_ , l’indicateur de progression est affichée à l’aide de l’implémentation de MAPI. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpInterface_
  
> [in] Un pointeur vers l’identificateur d’interface (IID) qui représente l’interface qui doit être utilisé pour accéder à l’objet indiqué par le paramètre _lpDestObj_ . Le paramètre _lpInterface_ ne doit pas être **null**.
    
 _lpDestObj_
  
> [in] Pointeur vers l’objet à recevoir les propriétés copiées ou déplacées.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis :
    
MAPI_DECLINE_OK 
  
> Si **CopyProps** appelle la méthode [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) pour gérer la copie ou l’opération de déplacement, il doit renvoyer immédiatement avec la valeur d’erreur MAPI_E_DECLINE_COPY. L’indicateur MAPI_DECLINE_OK est défini par MAPI pour limiter la récurrence. Les clients ne définissez pas cet indicateur. 
    
MAPI_DIALOG 
  
> Affiche un indicateur de progression.
    
MAPI_MOVE 
  
> **CopyProps** doit effectuer une opération de déplacement au lieu d’une opération de copie. Lorsque cet indicateur n’est pas défini, **CopyProps** effectue une opération de copie. 
    
MAPI_NOREPLACE 
  
> Propriétés existantes dans l’objet de destination ne doivent pas être remplacées. Lorsque cet indicateur n’est pas défini, **CopyProps** remplace les propriétés existantes. 
    
 _lppProblems_
  
> [entrée, sortie] À l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; Sinon, **valeur null**, indiquant qu’il n’a pas besoin d’informations sur l’erreur. Si _lppProblems_ est un pointeur valid en entrée, **CopyProps** renvoie des informations détaillées sur les erreurs lors de la copie d’une ou plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les propriétés ont été copiées ou déplacées.
    
MAPI_E_COLLISION 
  
> Un sous-objet ne peut pas être copié, car il existe déjà un sous-objet portant le même nom complet, défini par la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), dans l’objet de destination. 
    
MAPI_E_DECLINE_COPY 
  
> Le fournisseur de services n’implémente pas l’opération de copie.
    
MAPI_E_FOLDER_CYCLE 
  
> L’objet source de l’opération de copie ou déplacement directement ou indirectement contient l’objet de destination. Travail significatifs peut-être avoir été effectué avant cette condition a été détectée, et les objets source et de destination peuvent être modifiées partiellement. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L’interface identifié par le paramètre _lpInterface_ n’est pas pris en charge par l’objet de destination. 
    
MAPI_E_NO_ACCESS 
  
> Une tentative a été effectuée pour accéder à un objet pour lequel l’appelant dispose d’autorisations insuffisantes. Cette erreur est renvoyée si l’objet de destination est identique à l’objet source.
    
Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas en tant que valeurs de retour pour **CopyProps**. Ces erreurs s’appliquent à une propriété unique.
  
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et **CopyProps** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **CopyProps** prend en charge Unicode uniquement. 
    
MAPI_E_COMPUTED 
  
> La propriété ne peut pas être modifiée par l’appelant car il s’agit d’une propriété en lecture seule, calculée par le propriétaire de l’objet de destination. Cette erreur n’est pas lourde ; l’appelant doit autoriser l’opération de copie continuer.
    
MAPI_E_INVALID_TYPE 
  
> Le type de propriété n’est pas valide.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Le type de propriété n’est pas le type attendu par l’appelant.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::CopyProps** copie ou déplace les propriétés sélectionnées à partir de l’objet actif à un objet de destination. **CopyProps** est utilisé essentiellement pour répondre à et transférer des messages, où uniquement certaines des propriétés à partir du message d’origine se déplacent avec la réponse ou transférés copie. 
  
Les sous-objets de l’objet source sont automatiquement inclus dans l’opération et copiés ou déplacés dans son intégralité, indépendamment de l’utilisation des propriétés indiqués par la structure [SPropTagArray](sproptagarray.md) . Par défaut, **CopyProps** remplace toutes les propriétés de l’objet cible qui correspondent aux propriétés de l’objet source. Si les propriétés copiées ou déplacées existent déjà dans l’objet de destination, les propriétés existantes sont remplacées par les nouvelles propriétés, sauf si l’indicateur MAPI_NOREPLACE est défini dans le paramètre _ulFlags_ . Les informations existantes dans l’objet de destination n’est pas remplacé sont conservées. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Vous pouvez fournir une implémentation complète de **CopyProps** ou reposer sur l’implémentation MAPI fournit de l’objet de prise en charge. Si vous souhaitez utiliser l’implémentation MAPI, appelez la méthode **IMAPISupport::DoCopyProps** . Toutefois, si vous procédez comme déléguer le traitement de **DoCopyProps** et vous sont transmis à l’indicateur MAPI_DECLINE_OK, évitez l’appel de la prise en charge et renvoyer MAPI_E_DECLINE_COPY au lieu de cela. Vous sera appelée avec cet indicateur par MAPI pour éviter la récurrence possible qui peut se produire lorsque vous copiez les dossiers. 
  
Étant donné que l’opération de copie peut être longue, vous devez afficher un indicateur de progression. Utilisez l’implémentation [IMAPIProgress](imapiprogressiunknown.md) qui est passée dans le paramètre _lpProgress_ , le cas échéant. Si _lpProgress_ est **null**, appelez la méthode [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) pour utiliser l’implémentation MAPI. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Ne définissez pas l’indicateur MAPI_DECLINE_OK ; Il est utilisé par MAPI dans ses appels vers le message implémentations de **CopyProps** fournisseur de banque d’informations. 
  
Étant donné que les opérations de déplacement et de copie peuvent prendre le temps, il est judicieux de demander l’affichage d’un indicateur de progression en définissant l’indicateur MAPI_DIALOG. Vous pouvez définir le paramètre _lpProgress_ votre implémentation **IMAPIProgress**, si vous en avez un, ou **null**. Si _lpProgress_ est **null**, **CopyProps** utilisera l’indicateur de progression par défaut fourni par MAPI. 
  
Vous pouvez supprimer l’affichage d’un indicateur de progression en définissant ne pas l’indicateur MAPI_DIALOG. **CopyProps** ignorera les paramètres _ulUIParam_ et _lpProgress_ et éviter l’affichage de l’indicateur. 
  
 **CopyProps** peuvent signaler des erreurs globaux et individuels ou des erreurs qui se produisent avec un ou plusieurs des propriétés. Ces erreurs individuels sont placés dans une structure **SPropProblemArray** . Vous pouvez supprimer le rapport d’erreurs au niveau de la propriété en passant **null**, au lieu d’un pointeur valide, pour le paramètre property problème tableau structure. 
  
Si vous souhaitez recevoir des informations sur les erreurs, passez un pointeur de structure **SPropProblemArray** valid dans le paramètre _lppProblems_ . Lorsque **CopyProps** renvoie S_OK, vérifiez les erreurs possibles avec des propriétés individuelles dans la structure. **CopyProps** retourne une erreur, aucune information n’est retournée dans la structure **SPropProblemArray** . Au lieu de cela, appelez la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) pour récupérer des informations d’erreur détaillé. 
  
Si **CopyProps** renvoie S_OK, libérer la structure **SPropProblemArray** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si vous copiez les propriétés qui sont uniques pour le type d’objet source, assurez-vous que l’objet de destination est du même type. **CopyProps** ne vous empêche pas d’associant des propriétés qui appartiennent généralement à un type d’objet avec un autre type d’objet. C’est à vous pour copier des propriétés qui sont pertinents pour l’objet de destination. Par exemple, vous devez copier pas les propriétés de message à un conteneur de carnet d’adresses. 
  
Pour vous assurer que vous copiez entre les objets du même type, vérifiez que l’objet source et de destination sont le même type, par comparaison des pointeurs d’objet ou d’appeler la méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) . Définir l’identificateur d’interface désigné par _lpInterface_ à l’interface standard pour l’objet source. Vérifiez également que le type d’objet ou la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) est la même pour les deux objets. Par exemple, si vous copiez à partir d’un message, définissez _lpInterface_ IID_IMessage et le **PR_OBJECT_TYPE** pour les deux objets MAPI_MESSAGE. 
  
Si un pointeur non valide est passé dans le paramètre _lpDestObj_ , le résultat est imprévisible. 
  
Pour copier la liste des destinataires d’un message, appelez la méthode **CopyProps** du message et inclure la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans le tableau de balise de propriété. Pour copier les pièces jointes du message, inclure la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Pour copier un dossier une hiérarchie de conteneur de carnet adresses ou table des matières, incluez la **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou des propriétés de **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans le tableau de balise de propriété. Pour inclure la table du contenu associé d’un dossier, inclure la propriété **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) dans le tableau. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI utilise la méthode **IMAPIProp::CopyProps** pour copier des propriétés nommées à partir d’un message à un autre.  <br/> |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |MFCMAPI utilise la méthode **IMAPIProp::CopyProps** pour coller une propriété qui a été copiée à partir d’un autre objet.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
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

