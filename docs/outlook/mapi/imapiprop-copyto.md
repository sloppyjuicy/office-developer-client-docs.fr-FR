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
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356391"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace toutes les propriétés, à l'exception des propriétés spécifiquement exclues.
  
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
  
> dans Nombre d'interfaces à exclure lorsque les propriétés sont copiées ou déplacées.
    
 _rgiidExclude_
  
> dans Tableau des identificateurs d'interface (IID) qui spécifient les interfaces qui ne doivent pas être utilisées lorsque des informations supplémentaires sont copiées ou déplacées vers l'objet de destination.
    
 _lpExcludeProps_
  
> dans Pointeur vers un tableau de balises de propriété qui identifie les balises de propriété qui doivent être exclues de l'opération de copie ou de déplacement. Le fait de transmettre **null** dans le paramètre _lpExcludeProps_ indique que toutes les propriétés de l'objet doivent être copiées ou déplacées. **CopyTo** renvoie MAPI_E_INVALID_PARAMETER lorsque le membre **cValues** de la structure [SPropProblemArray](spropproblemarray.md) vers laquelle pointe _lpExcludeProps_ est défini sur 0. 
    
 _ulUIParam_
  
> dans Handle de la fenêtre parent de l'indicateur de progression. 
    
 _lpProgress_
  
> dans Pointeur vers une implémentation d'indicateur de progression. Si **null** est transmis dans le paramètre _lpProgress_ , MAPI fournit l'implémentation de la progression. Le paramètre _lpProgress_ est ignoré sauf si l'indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à l'objet pointé par le paramètre _lpDestObj_ . Le paramètre _lpInterface_ ne doit pas être **null**.
    
 _lpDestObj_
  
> dans Pointeur vers l'objet pour recevoir les propriétés copiées ou déplacées.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle l'opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis:
    
MAPI_DECLINE_OK 
  
> Si **CopyTo** appelle la méthode [IMAPISupport::D ocopyto](imapisupport-docopyto.md) pour gérer l'opération de copie ou de déplacement, il doit renvoyer immédiatement immédiatement la valeur d'erreur MAPI_E_DECLINE_COPY. L'indicateur MAPI_DECLINE_OK est défini par MAPI pour limiter la récursivité. Les clients ne définissent pas cet indicateur. 
    
MAPI_DIALOG 
  
> Affiche un indicateur de progression.
    
MAPI_MOVE 
  
> **CopyTo** doit effectuer une opération Move au lieu d'une opération de copie. Lorsque cet indicateur n'est pas défini, **CopyTo** effectue une opération de copie. 
    
MAPI_NOREPLACE 
  
> Les propriétés existantes dans l'objet de destination ne doivent pas être remplacées. Lorsque cet indicateur n'est pas défini, **CopyTo** remplace les propriétés existantes. 
    
 _lppProblems_
  
> [in, out] Lors de l'entrée, pointeur vers un pointeur vers une structure **SPropProblemArray** ; Sinon, **null**, indiquant qu'aucune information d'erreur n'est nécessaire. Si _lppProblems_ est un pointeur valide sur Input, **CopyTo** renvoie des informations détaillées sur les erreurs lors de la copie d'une ou de plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été correctement copiées ou déplacées.
    
MAPI_E_COLLISION 
  
> Un sous-objet ne peut pas être copié, car un sous-objet avec le même nom d'affichage, spécifié par la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), existe déjà dans l'objet de destination. 
    
MAPI_E_DECLINE_COPY 
  
> Le fournisseur de services n'implémente pas l'opération de copie.
    
MAPI_E_FOLDER_CYCLE 
  
> Objet source effectuant l'opération de copie ou de déplacement, directement ou indirectement, contenant l'objet de destination. Un travail significatif a pu être effectué avant la découverte de cette condition, de sorte que les objets source et de destination puissent être partiellement modifiés. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L'interface identifiée par le paramètre _lpInterface_ n'est pas prise en charge par l'objet de destination. 
    
MAPI_E_NO_ACCESS 
  
> Une tentative d'accès à un objet pour lequel l'appelant ne dispose pas des autorisations suffisantes a été effectuée. Cette erreur est renvoyée si l'objet de destination est identique à l'objet source.
    
Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas comme valeurs de retour pour **CopyTo**. Les erreurs suivantes s'appliquent à une seule propriété:
  
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et **CopyTo** ne prend pas en charge Unicode, ou MAPI_UNICODE n'est pas défini et **CopyTo** prend en charge uniquement Unicode. 
    
MAPI_E_COMPUTED 
  
> La propriété ne peut pas être modifiée par l'appelant car il s'agit d'une propriété en lecture seule, calculée par le propriétaire de l'objet de destination. Cette erreur n'est pas grave; l'appelant doit autoriser la poursuite de l'opération de copie.
    
MAPI_E_INVALID_TYPE 
  
> Le type de propriété n'est pas valide.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Le type de propriété n'est pas le type attendu par l'appelant.
    
## <a name="remarks"></a>Remarques

Par défaut, la méthode **IMAPIProp:: CopyTo** copie ou déplace toutes les propriétés de l'objet actif vers un objet de destination. **CopyTo** est utilisé lorsqu'un objet doit être copié ou déplacé exactement, avec toutes ou la plupart de ses propriétés intactes. 
  
Tous les sous-objets de l'objet source sont inclus automatiquement dans l'opération et sont copiés ou déplacés dans leur intégralité. Par défaut, **CopyTo** remplace toutes les propriétés de l'objet de destination qui correspondent aux propriétés de l'objet source. Si une des propriétés copiées ou déplacées existe déjà dans l'objet de destination, les propriétés existantes sont remplacées par les nouvelles propriétés, sauf si l'indicateur MAPI_NOREPLACE est défini dans le paramètre _ulFlags_ . Les informations existantes de l'objet de destination qui ne sont pas remplacées restent intactes. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez fournir une implémentation complète de **CopyTo** ou reposer sur l'implémentation fournie par MAPI dans son objet support. Si vous souhaitez utiliser l'implémentation MAPI, appelez **IMAPISupport::D ocopyto**. Toutefois, si vous déléguez le traitement à **DoCopyTo** et que vous avez passé l'indicateur MAPI_DECLINE_OK, évitez d'utiliser l'appel de prise en charge et de retourner MAPI_E_DECLINE_COPY à la place. MAPI appellera avec cet indicateur pour éviter la récursivité possible pouvant se produire lorsque les dossiers sont copiés. 
  
Étant donné que l'opération de copie peut être longue, vous devez afficher un indicateur de progression. Utilisez l'implémentation [méthode imapiprogress](imapiprogressiunknown.md) passée dans le paramètre _lpProgress_ , le cas échéant. Si _lpProgress_ est **null**, appelez la méthode [IMAPISupport::D OPROGRESSDIALOG](imapisupport-doprogressdialog.md) pour utiliser l'implémentation MAPI. 
  
N'essayez pas de définir des propriétés en lecture seule connues dans l'objet de destination; Retournez MAPI_E_NO_ACCESS à la place.
  
Les objets source et de destination doivent utiliser les mêmes interfaces. Renvoie MAPI_E_INVALID_PARAMETER si _lpInterface_ n'est pas défini. 
  
Renvoie MAPI_E_INTERFACE_NOT_SUPPORTED si toutes les interfaces connues sont exclues.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Ne définissez pas l'indicateur MAPI_DECLINE_OK; MAPI l'utilise dans ses appels aux implémentations du **** fournisseur de banque de messages. 
  
Étant donné que les opérations de copie et de déplacement peuvent prendre du temps, vous devez demander l'affichage d'un indicateur de progression en définissant l'indicateur MAPI_DIALOG. Vous pouvez définir le paramètre _lpProgress_ sur votre implémentation de **méthode imapiprogress**, si vous en avez un, ou sur **null**. Si _lpProgress_ a la **valeur null**, **CopyTo** utilise l'indicateur de progression par défaut fourni par MAPI. 
  
Vous pouvez supprimer l'affichage d'un indicateur de progression en ne définissant pas l'indicateur MAPI_DIALOG. **CopyTo** ignorera les paramètres _ulUIParam_ et _lpProgress_ et n'affichera pas l'indicateur. 
  
 **CopyTo** peut signaler des erreurs globales et individuelles, ou des erreurs qui se produisent avec une ou plusieurs propriétés. Ces erreurs individuelles sont placées dans une structure **SPropProblemArray** . Vous pouvez supprimer le rapport d'erreurs au niveau de la propriété en transférant **null**, au lieu d'un pointeur valide, pour le paramètre de structure de tableau de problèmes de propriété. 
  
Si vous souhaitez recevoir des informations sur les erreurs, transmettez un pointeur de structure **SPropProblemArray** valide dans le paramètre _lppProblems_ . Lorsque **CopyTo** renvoie S_OK, vérifiez la possibilité d'éventuelles erreurs avec des propriétés individuelles dans la structure. Lorsque **CopyTo** renvoie une erreur, aucune information n'est renvoyée dans la structure **SPropProblemArray** . Au lieu de cela, appelez [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) pour récupérer des informations détaillées sur l'erreur. 
  
Si **CopyTo** renvoie S_OK, libérez la structure **SPropProblemArray** renvoyée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si vous copiez des propriétés propres au type d'objet source, vous devez vous assurer que l'objet de destination est du même type. **CopyTo** ne vous empêche pas d'associer des propriétés qui appartiennent généralement à un type d'objet avec un autre type d'objet. Il vous revient de copier les propriétés qui ont un sens pour l'objet de destination. Par exemple, vous ne devez pas copier les propriétés de message dans un conteneur de carnet d'adresses. 
  
Pour vous assurer d'effectuer une copie entre les objets du même type, vérifiez que l'objet source et de destination sont du même type, soit en comparant des pointeurs d'objet, soit en appelant [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx). Définissez l'identificateur d'interface désigné par _lpInterface_ à l'interface standard pour l'objet source. Assurez-vous également que le type d'objet ou la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) est identique pour les deux objets. Par exemple, si vous copiez à partir d'un message, définissez _lpInterface_ sur IID_IMessage et le **PR_OBJECT_TYPE** pour les deux objets sur MAPI_MESSAGE. 
  
Si un pointeur non valide est transmis dans le paramètre _lpDestObj_ , les résultats sont imprévisibles. 
  
L'exclusion des propriétés d'un appel **CopyTo** peut être utile. Par exemple, certains objets ont des propriétés qui sont spécifiques à une seule instance de l'objet, telles que la date et l'heure de remise du message. Pour éviter de copier le délai de remise d'un message lorsque vous copiez le message dans un autre dossier, spécifiez **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) dans la balise de propriété Exclude Array. Pour exclure la liste de destinataires d'un message, ajoutez la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) au tableau d'exclusion. Pour exclure les pièces jointes d'un message, ajoutez la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) au tableau.
  
De même, vous empêchez la copie ou le changement de la table des matières ou de la hiérarchie d'un dossier ou d'un conteneur de carnet d'adresses en incluant **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans la balise de propriété Exclude Array.
  
Pour exclure les propriétés de l'opération de copie ou de déplacement, incluez les balises de propriété dans le paramètre _lpExcludeProps_ . Si vous transmettez les résultats de la macro **PROP_TAG** pour créer une balise de propriété à partir d'un identificateur spécifique dans le tableau de balises de propriété, toutes les propriétés dotées de cet identificateur seront exclues. Par exemple, l'entrée suivante dans le tableau de la balise de propriété entraîne l'exclusion de toutes les propriétés dotées d'un identificateur 0x8002, quel que soit le type: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
La balise de propriété **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ne peut pas être incluse dans le tableau _lpExcludeProps_ . 
  
L'utilité de la fonctionnalité **CopyTo** pour l'exclusion d'interfaces n'est peut-être pas aussi évidente que l'exclusion des propriétés. Vous pouvez exclure une interface lorsque vous copiez vers un objet qui n'a aucune connaissance d'un groupe de propriétés. Par exemple, si vous copiez les propriétés d'un dossier vers une pièce jointe, les seules propriétés que la pièce jointe peut utiliser sont les propriétés génériques disponibles pour toute implémentation [IMAPIProp](imapipropiunknown.md) . En excluant [IMAPIFolder](imapifolderimapicontainer.md) de l'opération de copie, la pièce jointe ne reçoit pas les propriétés de dossier les plus spécifiques. 
  
Lorsque vous utilisez le paramètre _rgiidExclude_ pour exclure une interface, il exclut également toutes les interfaces dérivées de cette interface. Par exemple, si vous excluez [IMAPIContainer](imapicontainerimapiprop.md) , les dossiers ou les conteneurs du carnet d'adresses seront exclus, selon le type de fournisseur. N'excluez pas **IMAPIProp** ou [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) car un grand nombre d'interfaces dérivent de celles-ci. 
  
Ignore les erreurs MAPI_E_COMPUTED renvoyées dans la structure **SPropProblemArray** dans le paramètre _lppProblems_ . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File. cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI utilise la méthode **IMAPIProp:: CopyTo** pour copier les propriétés d'un fichier. MSG vers un objet [IMAPIMessageSite](imapimessagesiteiunknown.md) .  <br/> |
|FolderDlg. cpp  <br/> |CFolderDlg:: HandlePaste  <br/> |MFCMAPI utilise la méthode **IMAPIProp:: CopyTo** pour copier les propriétés d'un message source vers un message cible pendant une opération de collage.  <br/> |
   
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

