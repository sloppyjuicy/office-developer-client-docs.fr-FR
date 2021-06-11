---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424454"
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

## <a name="parameters"></a>Parameters

 _lpMsgList_
  
> [in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui identifient le ou les messages à copier ou déplacer. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier de destination pointé par le paramètre _lpDestFolder._ La transmission de null entraîne le renvoi par le fournisseur de services de l’interface de dossier [standard, IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Les clients doivent transmettre la valeur NULL. D’autres appelants peuvent définir le paramètre  _lpInterface_ sur IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Pointeur vers le dossier ouvert pour recevoir les messages copiés ou déplacés.
    
 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode. Le _paramètre ulUIParam_ est ignoré, sauf si le client définit l’indicateur MESSAGE_DIALOG dans le paramètre _ulFlags_ et transmet null dans le paramètre _lpProgress._ 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est transmis dans  _lpProgress,_ le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le  _paramètre lpProgress est_ ignoré, sauf si l’MESSAGE_DIALOG est définie dans  _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’opération de copie ou de déplacement est accomplie. Les indicateurs suivants peuvent être définies :
    
MAPI_DECLINE_OK 
  
> Informe le fournisseur de la boutique de messages de renvoyer immédiatement MAPI_E_DECLINE_COPY s’il implémente **IMAPIFolder::CopyMessages** en appelant la méthode [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) de l’objet de support. 
    
MESSAGE_DIALOG 
  
> Affiche un indicateur de progression au cours de l’opération.
    
MESSAGE_MOVE 
  
> Le ou les messages doivent être déplacés au lieu d’être copiés. Si MESSAGE_MOVE n’est pas définie, les messages sont copiés.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le ou les messages ont été correctement copiés ou déplacés.
    
MAPI_E_DECLINE_COPY 
  
> Le fournisseur implémente cette méthode en appelant une méthode objet de support, et l’appelant a passé l’MAPI_DECLINE_OK’indicateur.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais toutes les entrées n’ont pas été correctement copiées ou déplacées. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIFolder::CopyMessages** copie ou déplace les messages vers un autre dossier. 
  
Les messages ouverts avec une autorisation de lecture/écriture peuvent être déplacés ou copiés. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous copiez des messages dans une autre magasin de messages sans utiliser la méthode [IMAPISupport::CopyMessages,](imapisupport-copymessages.md) vous devez d’abord appeler [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) avec l’indicateur GENERATE_RECEIPT_ONLY définie. La boutique de messages de réception n’est pas chargée de générer des rapports de lecture pour les messages copiés ou déplacés. Si vous appelez **IMAPISupport::CopyMessages** pour implémenter **IMAPIFolder::CopyMessages**, n’appelez **pas SetReadFlags**; MAPI l’appelle. 
  
Votre implémentation peut déplacer ou copier les messages dans n’importe quel ordre et générer des rapports d’état de lecture dans n’importe quel ordre. Autrement dit, vous pouvez terminer la copie des messages avant de générer les rapports d’état de lecture ou envoyer les rapports avant que votre implémentation ne démarre l’opération de copie. Toutefois, les rapports de lecture doivent être envoyés pour que tous les messages soient copiés, que la copie réussisse ou non.
  
Lorsque l’opération de copie ou de déplacement implique plusieurs messages, effectuez l’opération aussi complètement que possible. N’arrêtez pas l’opération prématurément, sauf si une défaillance dépasse votre contrôle, par exemple un manque de mémoire, un manque d’espace disque ou une altération de la magasin de messages.
  
Essayez de conserver les identificateurs d’entrée dans les opérations de déplacement ou de copie. Vous devez également conserver les identificateurs d’entrée, bien que cela ne soit pas obligatoire.
  
Envoyez des notifications lorsque vous déplacez ou copiez des messages afin que les clients soient avertis que leurs appels aux méthodes [IMAPIProp::SaveChanges](imapiprop-savechanges.md) des messages risquent d’échouer. 
  
N’incluez pas l’état d’un message dans l’opération de copie ou de déplacement. Le déplacement ou la copie de l’état d’un message affecte grandement les performances.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Utilisez **IMAPIFolder::CopyMessages** pour remplir les dossiers de résultats de recherche, où les messages sont souvent regroupés par dossier parent. 
  
Attendez-vous à ce que ces valeurs de retour se placent dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages** a correctement copié ou déplacé chaque message.  <br/> |S_OK  <br/> |
|**IMAPIFolder::CopyMessages** n’a pas pu copier ou déplacer tous les messages.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder::CopyMessages** n’a pas pu se terminer.  <br/> |Toute valeur d’erreur  <br/> |
   
Lorsque **IMAPIFolder::CopyMessages** n’est pas en mesure de se terminer, ne supposez pas qu’aucun travail n’a été effectué. **IMAPIFolder::CopyMessages** a peut-être pu copier ou déplacer un ou plusieurs messages avant de rencontrer l’erreur. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

