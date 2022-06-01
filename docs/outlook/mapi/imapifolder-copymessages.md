---
title: IMAPIFolderCopyMessages
description: IMAPIFolderCopyMessages copie ou déplace un ou plusieurs messages. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
ms.openlocfilehash: cadbffbf6156f7eaa1a3e4904173f1e8d33afc08
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816184"
---
# <a name="imapifoldercopymessages"></a>IMAPIFolder::CopyMessages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie ou déplace un ou plusieurs messages.
  
```cpp
HRESULT CopyMessages(
  LPENTRYLIST lpMsgList,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpMsgList_
  
> [in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui identifient le ou les messages à copier ou à déplacer. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier de destination pointé par le paramètre  _lpDestFolder_ . La transmission de la valeur NULL entraîne le retour par le fournisseur de services de l’interface de dossier standard [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Les clients doivent passer null. D’autres appelants peuvent définir le paramètre  _lpInterface_ sur IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Pointeur vers le dossier ouvert pour recevoir les messages copiés ou déplacés.
    
 _ulUIParam_
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode. Le paramètre  _ulUIParam_ est ignoré, sauf si le client définit l’indicateur MESSAGE_DIALOG dans le paramètre _ulFlags_ et passe null dans le paramètre _lpProgress_ . 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si null est passé dans  _lpProgress_, le fournisseur du magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le paramètre  _lpProgress_ est ignoré, sauf si l’indicateur MESSAGE_DIALOG est défini dans  _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’opération de copie ou de déplacement est effectuée. Les indicateurs suivants peuvent être définis :
    
MAPI_DECLINE_OK 
  
> Indique au fournisseur du magasin de messages de retourner immédiatement MAPI_E_DECLINE_COPY s’il **implémente IMAPIFolder::CopyMessages** en appelant la méthode [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::D oCopyProps de l’objet](imapisupport-docopyprops.md) de support. 
    
MESSAGE_DIALOG 
  
> Affiche un indicateur de progression à mesure que l’opération se poursuit.
    
MESSAGE_MOVE 
  
> Le ou les messages doivent être déplacés au lieu d’être copiés. Si MESSAGE_MOVE n’est pas défini, les messages sont copiés.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le ou les messages ont été correctement copiés ou déplacés.
    
MAPI_E_DECLINE_COPY 
  
> Le fournisseur implémente cette méthode en appelant une méthode objet de support, et l’appelant a passé l’indicateur MAPI_DECLINE_OK.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais toutes les entrées n’ont pas été correctement copiées ou déplacées. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::CopyMessages** copie ou déplace les messages vers un autre dossier. 
  
Les messages ouverts avec une autorisation de lecture/écriture peuvent être déplacés ou copiés. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous copiez des messages vers un autre magasin de messages sans utiliser la méthode [IMAPISupport::CopyMessages](imapisupport-copymessages.md) , vous devez d’abord appeler [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) avec l’indicateur GENERATE_RECEIPT_ONLY défini. Le magasin de messages de réception n’est pas responsable de la génération de rapports de lecture pour les messages copiés ou déplacés. Si vous appelez **IMAPISupport::CopyMessages** pour **implémenter IMAPIFolder::CopyMessages**, n’appelez pas **SetReadFlags** ; MAPI l’appellera. 
  
Votre implémentation peut déplacer ou copier les messages dans n’importe quel ordre et générer des rapports d’état de lecture dans n’importe quel ordre. Autrement dit, vous pouvez terminer la copie des messages avant de générer l’un des rapports d’état de lecture ou d’envoyer les rapports avant que votre implémentation ne démarre l’opération de copie. Toutefois, les rapports de lecture doivent être envoyés pour que tous les messages soient copiés, que la copie soit réussie ou non.
  
Lorsque l’opération de copie ou de déplacement implique plusieurs messages, effectuez l’opération aussi complètement que possible. N’arrêtez pas l’opération prématurément, à moins qu’une défaillance ne soit hors de votre contrôle, comme un manque de mémoire, un manque d’espace disque ou une altération du magasin de messages.
  
Essayez de conserver les identificateurs d’entrée dans les opérations de déplacement ou de copie. Vous devez également conserver les identificateurs d’entrée, bien qu’il ne soit pas obligatoire.
  
Envoyez des notifications lorsque vous déplacez ou copiez des messages afin que les clients soient avertis que leurs appels aux méthodes [IMAPIProp::SaveChanges](imapiprop-savechanges.md) des messages peuvent échouer. 
  
N’incluez pas l’état d’un message dans l’opération de copie ou de déplacement. Le déplacement ou la copie d’un état de message affecte considérablement les performances.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Utilisez **IMAPIFolder::CopyMessages** pour remplir les dossiers de résultats de recherche, où les messages sont souvent regroupés par dossier parent. 
  
Attendez-vous à ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages** a correctement copié ou déplacé chaque message. |S_OK  <br/> |
|**IMAPIFolder::CopyMessages** n’a pas pu copier ou déplacer correctement chaque message. |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder::CopyMessages** n’a pas pu se terminer. |Toute valeur d’erreur  <br/> |
   
Lorsque **IMAPIFolder::CopyMessages** ne peut pas se terminer, ne partez pas du principe qu’aucun travail n’a été effectué. **IMAPIFolder::CopyMessages** a peut-être pu copier ou déplacer un ou plusieurs messages avant de rencontrer l’erreur. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

