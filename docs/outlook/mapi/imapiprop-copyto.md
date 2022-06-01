---
title: IMAPIPropCopyTo
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPIPropCopyTo, qui copie ou déplace toutes les propriétés, à l’exception des propriétés spécifiquement exclues.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
ms.openlocfilehash: 288035d60d1bbfa9421c1e2e98483f26e3e8a149
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816611"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace toutes les propriétés, à l’exception des propriétés spécifiquement exclues.
  
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
  
> [in] Nombre d’interfaces à exclure lorsque les propriétés sont copiées ou déplacées.
    
 _rgiidExclude_
  
> [in] Tableau d’identificateurs d’interface (IID) qui spécifient des interfaces qui ne doivent pas être utilisées lorsque des informations supplémentaires sont copiées ou déplacées vers l’objet de destination.
    
 _lpExcludeProps_
  
> [in] Pointeur vers un tableau de balises de propriétés qui identifie les balises de propriété qui doivent être exclues de l’opération de copie ou de déplacement. Le passage de **la valeur null** dans le paramètre _lpExcludeProps_ indique que toutes les propriétés de l’objet doivent être copiées ou déplacées. **CopyTo** retourne MAPI_E_INVALID_PARAMETER lorsque le membre **cValues** de la structure [SPropProblemArray](spropproblemarray.md) pointée par  _lpExcludeProps_ est défini sur 0. 
    
 _ulUIParam_
  
> [in] Handle de la fenêtre parente de l’indicateur de progression. 
    
 _lpProgress_
  
> [in] Pointeur vers une implémentation d’indicateur de progression. Si **null** est passé dans le paramètre _lpProgress_ , MAPI fournit l’implémentation de progression. Le paramètre  _lpProgress_ est ignoré, sauf si l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet pointé par le paramètre  _lpDestObj_ . Le paramètre  _lpInterface_ ne doit pas être **null**.
    
 _lpDestObj_
  
> [in] Pointeur vers l’objet pour recevoir les propriétés copiées ou déplacées.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis :
    
MAPI_DECLINE_OK 
  
> Si **CopyTo** appelle la méthode [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) pour gérer l’opération de copie ou de déplacement, elle doit retourner immédiatement avec la valeur d’erreur MAPI_E_DECLINE_COPY. L’indicateur MAPI_DECLINE_OK est défini par MAPI pour limiter la récursivité. Les clients ne définissent pas cet indicateur. 
    
MAPI_DIALOG 
  
> Affiche un indicateur de progression.
    
MAPI_MOVE 
  
> **CopyTo** doit effectuer une opération de déplacement au lieu d’une opération de copie. Lorsque cet indicateur n’est pas défini, **CopyTo** effectue une opération de copie. 
    
MAPI_NOREPLACE 
  
> Les propriétés existantes dans l’objet de destination ne doivent pas être remplacées. Lorsque cet indicateur n’est pas défini, **CopyTo** remplace les propriétés existantes. 
    
 _lppProblems_
  
> [in, out] Lors de l’entrée, un pointeur vers un pointeur vers une structure **SPropProblemArray** ; sinon, **null**, indiquant qu’aucune information d’erreur n’est nécessaire. Si  _lppProblems_ est un pointeur valide sur l’entrée, **CopyTo** retourne des informations détaillées sur les erreurs de copie d’une ou plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été correctement copiées ou déplacées.
    
MAPI_E_COLLISION 
  
> Impossible de copier un sous-objet, car un sous-objet portant le même nom d’affichage , spécifié par la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), existe déjà dans l’objet de destination. 
    
MAPI_E_DECLINE_COPY 
  
> Le fournisseur de services n’implémente pas l’opération de copie.
    
MAPI_E_FOLDER_CYCLE 
  
> L’objet source effectuant l’opération de copie ou de déplacement contient directement ou indirectement l’objet de destination. Un travail important peut avoir été effectué avant la découverte de cette condition, de sorte que les objets source et de destination peuvent être partiellement modifiés. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L’interface identifiée par le paramètre  _lpInterface_ n’est pas prise en charge par l’objet de destination. 
    
MAPI_E_NO_ACCESS 
  
> Une tentative d’accès à un objet pour lequel l’appelant dispose d’autorisations insuffisantes a été effectuée. Cette erreur est retournée si l’objet de destination est identique à l’objet source.
    
Les valeurs suivantes peuvent être retournées dans la structure **SPropProblemArray** , mais pas en tant que valeurs de retour pour **CopyTo**. Les erreurs suivantes s’appliquent à une seule propriété :
  
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et **CopyTo** ne prend pas en charge Unicode, soit MAPI_UNICODE n’a pas été défini et **CopyTo** prend uniquement en charge Unicode. 
    
MAPI_E_COMPUTED 
  
> La propriété ne peut pas être modifiée par l’appelant, car il s’agit d’une propriété en lecture seule, calculée par le propriétaire de l’objet de destination. Cette erreur n’est pas grave; l’appelant doit autoriser la poursuite de l’opération de copie.
    
MAPI_E_INVALID_TYPE 
  
> Le type de propriété n’est pas valide.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Le type de propriété n’est pas le type attendu par l’appelant.
    
## <a name="remarks"></a>Remarques

Par défaut, la méthode **IMAPIProp::CopyTo** copie ou déplace toutes les propriétés de l’objet actuel vers un objet de destination. **CopyTo** est utilisé lorsqu’un objet doit être copié ou déplacé exactement, avec la totalité ou la plupart de ses propriétés intactes. 
  
Tous les sous-objets de l’objet source sont automatiquement inclus dans l’opération et sont copiés ou déplacés dans leur intégralité. Par défaut, **CopyTo** remplace toutes les propriétés de l’objet de destination qui correspondent aux propriétés de l’objet source. Si l’une des propriétés copiées ou déplacées existe déjà dans l’objet de destination, les propriétés existantes sont remplacées par les nouvelles propriétés, sauf si l’indicateur MAPI_NOREPLACE est défini dans le paramètre _ulFlags_ . Les informations existantes dans l’objet de destination qui ne sont pas remplacées restent intactes. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez fournir une implémentation complète de **CopyTo** ou vous appuyer sur l’implémentation fournie par MAPI dans son objet de support. Si vous souhaitez utiliser l’implémentation MAPI, appelez **IMAPISupport::D oCopyTo**. Toutefois, si vous déléguez le traitement à **DoCopyTo** et que vous avez passé l’indicateur MAPI_DECLINE_OK, évitez l’appel de support et retournez MAPI_E_DECLINE_COPY à la place. MAPI appelle avec cet indicateur pour éviter la récursivité possible qui peut se produire lorsque des dossiers sont copiés. 
  
Étant donné que l’opération de copie peut être longue, vous devez afficher un indicateur de progression. Utilisez l’implémentation [IMAPIProgress](imapiprogressiunknown.md) passée dans le paramètre _lpProgress_ , le cas échéant. Si  _lpProgress_ a la valeur **Null**, appelez la méthode [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) pour utiliser l’implémentation MAPI. 
  
Ne tentez pas de définir des propriétés connues en lecture seule dans l’objet de destination ; retourner MAPI_E_NO_ACCESS à la place.
  
Les objets source et de destination doivent utiliser les mêmes interfaces. Retournez MAPI_E_INVALID_PARAMETER si  _lpInterface_ n’est pas défini. 
  
Retournez MAPI_E_INTERFACE_NOT_SUPPORTED si toutes les interfaces connues sont exclues.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Ne définissez pas l’indicateur de MAPI_DECLINE_OK ; MAPI l’utilise dans ses appels aux implémentations **copyTo** du fournisseur de magasin de messages. 
  
Étant donné que les opérations de copie et de déplacement peuvent prendre du temps, vous devez demander l’affichage d’un indicateur de progression en définissant l’indicateur MAPI_DIALOG. Vous pouvez définir le paramètre  _lpProgress_ sur votre implémentation **d’IMAPIProgress**, si vous en avez un, ou sur **null**. Si  _lpProgress_ a la valeur **Null**, **CopyTo** utilise l’indicateur de progression par défaut fourni par MAPI. 
  
Vous pouvez supprimer l’affichage d’un indicateur de progression en ne définissant pas l’indicateur MAPI_DIALOG. **CopyTo** ignore les paramètres  _ulUIParam_ et  _lpProgress_ et n’affiche pas l’indicateur. 
  
 **CopyTo** peut signaler des erreurs globales et individuelles, ou des erreurs qui se produisent avec une ou plusieurs propriétés. Ces erreurs individuelles sont placées dans une structure **SPropProblemArray** . Vous pouvez supprimer la création de rapports d’erreurs au niveau de la propriété en passant **la valeur Null**, au lieu d’un pointeur valide, pour le paramètre de structure du tableau de problèmes de propriétés. 
  
Si vous souhaitez recevoir des informations sur les erreurs, transmettez un pointeur de structure **SPropProblemArray** valide dans le paramètre _lppProblems_ . Lorsque **CopyTo** retourne S_OK, recherchez les erreurs possibles avec des propriétés individuelles dans la structure. Lorsque **CopyTo** retourne une erreur, aucune information n’est retournée dans la structure **SPropProblemArray** . Appelez plutôt [IMAPIProp::GetLastError](imapiprop-getlasterror.md) pour récupérer des informations détaillées sur l’erreur. 
  
Si **CopyTo** retourne S_OK, libérez la structure **SPropProblemArray** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si vous copiez des propriétés propres au type d’objet source, vous devez vous assurer que l’objet de destination est du même type. **CopyTo** ne vous empêche pas d’associer des propriétés qui appartiennent généralement à un type d’objet à un autre type d’objet. C’est à vous de copier les propriétés qui ont un sens pour l’objet de destination. Par exemple, vous ne devez pas copier les propriétés de message dans un conteneur de carnet d’adresses. 
  
Pour vous assurer de copier entre des objets du même type, vérifiez que l’objet source et l’objet de destination sont du même type, soit en comparant des pointeurs d’objet, soit [en appelant IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx). Définissez l’identificateur d’interface pointé par  _lpInterface_ sur l’interface standard pour l’objet source. Assurez-vous également que le type d’objet ou la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) est le même pour les deux objets. Par exemple, si vous copiez à partir d’un message, définissez  _lpInterface_ sur IID_IMessage et le **PR_OBJECT_TYPE** pour les deux objets sur MAPI_MESSAGE. 
  
Si un pointeur non valide est passé dans le paramètre _lpDestObj_ , les résultats sont imprévisibles. 
  
L’exclusion de propriétés sur un appel **CopyTo** peut être utile. Par exemple, certains objets ont des propriétés spécifiques à une seule instance de l’objet, telles que la date et l’heure de remise des messages. Pour éviter de copier le délai de remise d’un message lorsque vous copiez le message dans un autre dossier, spécifiez **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) dans le tableau d’exclusion de balise de propriété. Pour exclure la liste des destinataires d’un message, ajoutez la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) au tableau d’exclusion. Pour exclure les pièces jointes d’un message, ajoutez la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) au tableau.
  
De même, empêchez la copie ou le déplacement de la hiérarchie ou de la table de contenu d’un dossier ou d’un carnet d’adresses en incluant **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans le tableau d’exclusion de balise de propriété.
  
Pour exclure des propriétés de l’opération de copie ou de déplacement, incluez leurs balises de propriété dans le paramètre _lpExcludeProps_ . Si vous transmettez les résultats de la **macro PROP_TAG** pour générer une balise de propriété à partir d’un identificateur spécifique dans le tableau de balises de propriétés, toutes les propriétés avec cet identificateur sont exclues. Par exemple, l’entrée suivante dans le tableau de balises de propriétés entraîne l’exclusion de toutes les propriétés avec un identificateur de 0x8002, quel que soit le type : 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
La balise de propriété **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ne peut pas être incluse dans le tableau _lpExcludeProps_ . 
  
L’utilité de la fonctionnalité **CopyTo** pour exclure les interfaces n’est peut-être pas aussi évidente que l’utilité de l’exclusion des propriétés. Vous pouvez exclure une interface lorsque vous copiez vers un objet qui n’a aucune connaissance d’un groupe de propriétés. Par exemple, si vous copiez des propriétés d’un dossier vers une pièce jointe, les seules propriétés que la pièce jointe peut utiliser sont les propriétés génériques disponibles avec n’importe quelle implémentation [IMAPIProp](imapipropiunknown.md) . En excluant [IMAPIFolder](imapifolderimapicontainer.md) de l’opération de copie, la pièce jointe ne recevra aucune des propriétés de dossier les plus spécifiques. 
  
Lorsque vous utilisez le paramètre  _rgiidExclude_ pour exclure une interface, il exclut également toutes les interfaces dérivées de cette interface. Par exemple, l’exclusion [d’IMAPIContainer](imapicontainerimapiprop.md) entraîne l’exclusion des dossiers ou des conteneurs de carnets d’adresses, en fonction du type de fournisseur. N’excluez pas **IMAPIProp** ou [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) , car de nombreuses interfaces en dérivent. 
  
Ignorez MAPI_E_COMPUTED erreurs retournées dans la structure **SPropProblemArray** dans le paramètre _lppProblems_ . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI utilise la méthode **IMAPIProp::CopyTo** pour copier des propriétés d’un fichier .msg vers un objet [IMAPIMessageSite](imapimessagesiteiunknown.md) . |
|FolderDlg.cpp  <br/> |CFolderDlg::HandlePaste  <br/> |MFCMAPI utilise la méthode **IMAPIProp::CopyTo** pour copier des propriétés d’un message source vers un message cible pendant une opération de collage. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
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

