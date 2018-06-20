---
title: IMAPIPropCopyTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: aa2869b1e3495bfb8a431e79a55d11a1ee1c5ca6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783895"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**S’applique à**: Outlook 
  
Copie ou déplace toutes les propriétés, à l’exception de spécifiquement des propriétés exclues.
  
```cpp
HRESULT CopyTo(
 ULONG ciidExclude,
 LPCIID rgiidExclude,
 LPSPropTagArray lpExcludeProps,
 ULONG_PTR ulUIParam,
 LPMAPIPROGRESS lpProgress,
 LPCIID lpInterface,
 LPVOID lpDestObj,
 ULONG ulFlags,
 LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Paramètres

 _ciidExclude_
  
> [in] Le nombre d’interfaces à exclure des propriétés sont copiées ou déplacées.
    
 _rgiidExclude_
  
> [in] Tableau d’identificateurs d’interface (IID) qui spécifient les interfaces qui ne doivent pas être utilisées lorsque des informations supplémentaires sont copiées ou déplacées à l’objet de destination.
    
 _lpExcludeProps_
  
> [in] Pointeur vers un tableau de balise de propriété qui identifie les balises de propriété qui doivent être exclus de la copie ou l’opération de déplacement. Le passage de **null** dans le paramètre _lpExcludeProps_ indique que toutes les propriétés de l’objet doivent être copiés ou déplacés. **CopyTo** renvoie MAPI_E_INVALID_PARAMETER lorsque le membre **cValues** de la structure [SPropProblemArray](spropproblemarray.md) désignés par _lpExcludeProps_ est définie sur 0. 
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent de l’indicateur de progression. 
    
 _lpProgress_
  
> [in] Pointeur vers une implémentation d’indicateur de progression. Si la **valeur null** est passée dans le paramètre _lpProgress_ , MAPI fournit l’implémentation de progression. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpInterface_
  
> [in] Un pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet indiqué par le paramètre _lpDestObj_ . Le paramètre _lpInterface_ ne doit pas être **null**.
    
 _lpDestObj_
  
> [in] Pointeur vers l’objet à recevoir les propriétés copiées ou déplacées.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis :
    
MAPI_DECLINE_OK 
  
> Si **CopyTo** appelle la méthode [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) pour gérer la copie ou l’opération de déplacement, il doit renvoyer immédiatement avec la valeur d’erreur MAPI_E_DECLINE_COPY. L’indicateur MAPI_DECLINE_OK est défini par MAPI pour limiter la récurrence. Les clients ne définissez pas cet indicateur. 
    
MAPI_DIALOG 
  
> Affiche un indicateur de progression.
    
MAPI_MOVE 
  
> **CopyTo** doit effectuer une opération de déplacement au lieu d’une opération de copie. Lorsque cet indicateur n’est pas défini, **CopyTo** effectue une opération de copie. 
    
MAPI_NOREPLACE 
  
> Propriétés existantes dans l’objet de destination ne doivent pas être remplacées. Lorsque cet indicateur n’est pas défini, **CopyTo** remplace les propriétés existantes. 
    
 _lppProblems_
  
> [entrée, sortie] À l’entrée, un pointeur vers un pointeur vers une structure **SPropProblemArray** ; dans le cas contraire, **null**, indiquant ainsi pas besoin d’informations sur l’erreur. Si _lppProblems_ est un pointeur valid en entrée, **CopyTo** renvoie des informations détaillées sur les erreurs lors de la copie d’une ou plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les propriétés ont été copiées ou déplacées.
    
MAPI_E_COLLISION 
  
> Impossible de copier un sous-objet car un sous-objet ayant le même nom d’affichage, spécifiée par la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) — existe déjà dans l’objet de destination. 
    
MAPI_E_DECLINE_COPY 
  
> Le fournisseur de services n’implémente pas l’opération de copie.
    
MAPI_E_FOLDER_CYCLE 
  
> L’objet source de l’opération de copie ou déplacement directement ou indirectement contient l’objet de destination. Travail significatifs peut-être avoir été effectué avant cette condition a été détectée, et les objets source et de destination peuvent être modifiées partiellement. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L’interface identifié par le paramètre _lpInterface_ n’est pas pris en charge par l’objet de destination. 
    
MAPI_E_NO_ACCESS 
  
> Une tentative a été effectuée pour accéder à un objet pour lequel l’appelant dispose d’autorisations insuffisantes. Cette erreur est renvoyée si l’objet de destination est identique à l’objet source.
    
Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas en tant que valeurs de retour pour **CopyTo**. Les erreurs suivantes s’appliquent à une seule propriété :
  
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et **CopyTo** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **CopyTo** prend en charge Unicode uniquement. 
    
MAPI_E_COMPUTED 
  
> La propriété ne peut pas être modifiée par l’appelant car il s’agit d’une propriété en lecture seule, calculée par le propriétaire de l’objet de destination. Cette erreur n’est pas lourde ; l’appelant doit autoriser l’opération de copie continuer.
    
MAPI_E_INVALID_TYPE 
  
> Le type de propriété n’est pas valide.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Le type de propriété n’est pas le type attendu par l’appelant.
    
## <a name="remarks"></a>Remarques

Par défaut, la méthode **IMAPIProp::CopyTo** copie ou déplace toutes les propriétés de l’objet en cours à un objet de destination. **CopyTo** est utilisée lorsqu’un objet doit être copié ou déplacé exactement, avec tout ou partie de ses propriétés intactes. 
  
Les sous-objets de l’objet source sont automatiquement inclus dans l’opération et sont copiés ou déplacés dans leur intégralité. Par défaut, **CopyTo** remplace toutes les propriétés de l’objet cible qui correspondent aux propriétés de l’objet source. Si les propriétés copiées ou déplacées existent déjà dans l’objet de destination, les propriétés existantes sont remplacées par les nouvelles propriétés, sauf si l’indicateur MAPI_NOREPLACE est défini dans le paramètre _ulFlags_ . Les informations existantes dans l’objet de destination n’est pas remplacé sont conservées. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Vous pouvez fournir une implémentation complète de **CopyTo** ou reposer sur l’implémentation MAPI fournit de l’objet de prise en charge. Si vous souhaitez utiliser l’implémentation MAPI, appelez **IMAPISupport::DoCopyTo**. Toutefois, si vous procédez comme déléguer le traitement de **DoCopyTo** et vous sont transmis à l’indicateur MAPI_DECLINE_OK, évitez l’appel de la prise en charge et renvoyer MAPI_E_DECLINE_COPY au lieu de cela. MAPI appellera avec cet indicateur pour éviter la récurrence possible qui peut se produire lorsque les dossiers sont copiés. 
  
Étant donné que l’opération de copie peut être longue, vous devez afficher un indicateur de progression. Utilisez l’implémentation de [IMAPIProgress](imapiprogressiunknown.md) transmise dans le paramètre _lpProgress_ , le cas échéant. Si _lpProgress_ est **null**, appelez la méthode [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) pour utiliser l’implémentation MAPI. 
  
N’essayez pas de définir des propriétés en lecture seule connues dans l’objet de destination ; Retournez à la place MAPI_E_NO_ACCESS.
  
Les objets source et de destination doivent utiliser les mêmes interfaces. Retourner MAPI_E_INVALID_PARAMETER si _lpInterface_ n’est pas définie. 
  
Retourner MAPI_E_INTERFACE_NOT_SUPPORTED si toutes les interfaces connus sont exclus.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Ne définissez pas l’indicateur MAPI_DECLINE_OK ; MAPI utilise dans ses appels pour les implémentations de **CopyTo** de fournisseur de banque d’informations du message. 
  
Étant donné que les opérations de déplacement et de copie peuvent prendre un temps, vous devez demander l’affichage d’un indicateur de progression en définissant l’indicateur MAPI_DIALOG. Vous pouvez définir le paramètre _lpProgress_ votre implémentation **IMAPIProgress**, si vous en avez un, ou **null**. Si _lpProgress_ est **null**, **CopyTo** utilisera l’indicateur de progression par défaut offertes par MAPI. 
  
Vous pouvez supprimer l’affichage d’un indicateur de progression en définissant ne pas l’indicateur MAPI_DIALOG. **CopyTo** ignorera les paramètres _ulUIParam_ et _lpProgress_ et n’affiche pas l’indicateur. 
  
 **CopyTo** peuvent signaler des erreurs globaux et individuels ou des erreurs qui se produisent avec une ou plusieurs propriétés. Ces erreurs individuels sont placés dans une structure **SPropProblemArray** . Vous pouvez supprimer le rapport d’erreurs au niveau de la propriété en passant **null**, au lieu d’un pointeur valide, pour le paramètre property problème tableau structure. 
  
Si vous souhaitez recevoir des informations sur les erreurs, passez un pointeur de structure **SPropProblemArray** valid dans le paramètre _lppProblems_ . Lorsque **CopyTo** renvoie S_OK, vérifiez les erreurs possibles avec des propriétés individuelles dans la structure. **CopyTo** retourne une erreur, aucune information n’est retournée dans la structure **SPropProblemArray** . Au lieu de cela, appelez [IMAPIProp::GetLastError](imapiprop-getlasterror.md) pour récupérer des informations d’erreur détaillé. 
  
Si **CopyTo** renvoie S_OK, libérer la structure **SPropProblemArray** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si vous copiez les propriétés qui sont uniques pour le type d’objet source, vous devez vous assurer que l’objet de destination est du même type. **CopyTo** ne vous empêche pas d’associant des propriétés qui appartiennent généralement à un type d’objet avec un autre type d’objet. C’est à vous pour copier des propriétés qui sont pertinents pour l’objet de destination. Par exemple, vous devez copier pas les propriétés de message à un conteneur de carnet d’adresses. 
  
Pour vous assurer que vous copiez entre les objets du même type, vérifiez que l’objet source et de destination sont le même type, soit en comparaison des pointeurs d’objet ou en appelant [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx). Définir l’identificateur d’interface désigné par _lpInterface_ à l’interface standard pour l’objet source. En outre, n’oubliez pas que le type d’objet ou la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) est la même pour les deux objets. Par exemple, si vous copiez à partir d’un message, définissez _lpInterface_ IID_IMessage et le **PR_OBJECT_TYPE** pour les deux objets MAPI_MESSAGE. 
  
Si un pointeur non valide est passé dans le paramètre _lpDestObj_ , le résultat est imprévisible. 
  
Exclusion des propriétés sur un appel **CopyTo** peuvent être utile. Par exemple, certains objets ont des propriétés qui sont spécifiques à une seule instance de l’objet, telles que la date et l’heure de remise du message. Pour éviter de copier l’heure de remise d’un message lorsque vous copiez le message vers un autre dossier, spécifiez **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) dans la propriété tag exclure le tableau. Pour exclure la liste des destinataires d’un message, ajoutez la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans le tableau exclure. Pour exclure les pièces jointes d’un message, ajoutez la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) dans le tableau.
  
De même, empêcher la copie ou le déplacement d’un dossier ou une table de hiérarchie ou le contenu du conteneur de carnet d’adresses en incluant **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans la propriété tag exclure tableau.
  
Pour exclure les propriétés de la copie ou l’opération de déplacement, inclut les balises de propriété dans le paramètre _lpExcludeProps_ . Si vous passez les résultats de la macro **PROP_TAG** pour créer une balise de propriété à partir d’un identificateur spécifique dans le tableau de balise de propriété, toutes les propriétés de cet identificateur seront exclues. Par exemple, l’entrée suivante dans le tableau de la propriété tag, toutes les propriétés d’un identificateur de 0x8002 à exclure, quel que soit le type : 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
La balise de propriété **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ne peut pas être incluse dans le tableau _lpExcludeProps_ . 
  
L’utilité de la fonctionnalité **CopyTo** pour exclure des interfaces n’est peut-être pas comme évidente comme l’utilité de l’exclusion des propriétés. Vous pouvez exclure une interface lors de la copie à un objet qui n’a pas connaissance d’un groupe de propriétés. Par exemple, si vous copiez les propriétés d’un dossier à une pièce jointe, les seules propriétés fonctionnant avec la pièce jointe sont les propriétés génériques disponibles avec n’importe quelle implémentation [IMAPIProp](imapipropiunknown.md) . En excluant [IMAPIFolder](imapifolderimapicontainer.md) à partir de l’opération de copie, la pièce jointe ne reçoit pas toutes les propriétés de dossier plus spécifiques. 
  
Lorsque vous utilisez le paramètre _rgiidExclude_ pour exclure une interface, il exclut également toutes les interfaces dérivées de cette interface. Par exemple, à l’exclusion de [IMAPIContainer](imapicontainerimapiprop.md) , dossiers ou conteneurs de carnet d’adresses à exclure, selon le type de fournisseur. N’excluent pas **IMAPIProp** ou [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) , car les interfaces autant dérivent de ces derniers. 
  
MAPI_E_COMPUTED ignorer les erreurs renvoyées dans la structure **SPropProblemArray** dans le paramètre _lppProblems_ . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI utilise la méthode **IMAPIProp::CopyTo** pour copier les propriétés d’un fichier .msg à un objet [IMAPIMessageSite](imapimessagesiteiunknown.md) .  <br/> |
|FolderDlg.cpp  <br/> |CFolderDlg::HandlePaste  <br/> |MFCMAPI utilise la méthode **IMAPIProp::CopyTo** pour copier les propriétés d’un message source vers un message cible pendant une opération de collage.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propriété canonique PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propriété canonique PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propriété canonique PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)
  
[Propriété canonique PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[Propriété canonique PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

