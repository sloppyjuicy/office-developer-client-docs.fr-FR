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

## <a name="parameters"></a>Paramètres

 _lpMsgList_
  
> dans Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui identifient le ou les messages à copier ou déplacer. 
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder au dossier de destination pointé par le paramètre _lpDestFolder_ . Le transfert de la valeur NULL entraîne le renvoi de l'interface de dossier standard [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Les clients doivent transmettre la valeur NULL. Les autres appelants peuvent définir le paramètre _lpInterface_ sur IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> dans Pointeur vers le dossier ouvert qui reçoit les messages copiés ou déplacés.
    
 _ulUIParam_
  
> dans Handle de la fenêtre parente de toutes les boîtes de dialogue ou fenêtres que cette méthode affiche. Le paramètre _ulUIParam_ est ignoré sauf si le client définit l'indicateur MESSAGE_DIALOG dans le paramètre _ULFLAGS_ et transmet null dans le paramètre _lpProgress_ . 
    
 _lpProgress_
  
> dans Pointeur vers un objet de progression qui affiche un indicateur de progression. Si la valeur NULL est transmise dans _lpProgress_, le fournisseur de banque de messages affiche un indicateur de progression à l'aide de l'implémentation de l'objet de progression MAPI. Le paramètre _lpProgress_ est ignoré sauf si l'indicateur MESSAGE_DIALOG est défini dans _ulFlags_.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'exécution de l'opération de copie ou de déplacement. Les indicateurs suivants peuvent être définis:
    
MAPI_DECLINE_OK 
  
> Informe le fournisseur de banque de messages pour qu'il renvoie immédiatement MAPI_E_DECLINE_COPY s'il implémente **IMAPIFolder:: CopyMessages** en appelant la méthode [IMAPISupport::D ocopyto](imapisupport-docopyto.md) ou [IMAPISupport::D](imapisupport-docopyprops.md) ocopyprops de l'objet de prise en charge. 
    
MESSAGE_DIALOG 
  
> Affiche un indicateur de progression pendant l'exécution de l'opération.
    
MESSAGE_MOVE 
  
> Le ou les messages doivent être déplacés au lieu d'être copiés. Si MESSAGE_MOVE n'est pas défini, les messages sont copiés.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le ou les messages ont été correctement copiés ou déplacés.
    
MAPI_E_DECLINE_COPY 
  
> Le fournisseur implémente cette méthode en appelant une méthode d'objet de prise en charge, et l'appelant a passé l'indicateur MAPI_DECLINE_OK.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L'appel a réussi, mais certaines entrées n'ont pas été correctement copiées ou déplacées. Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder:: CopyMessages** copie ou déplace les messages vers un autre dossier. 
  
Les messages ouverts avec une autorisation en lecture/écriture peuvent être déplacés ou copiés. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous copiez des messages vers une autre banque de messages sans utiliser la méthode [IMAPISupport:: CopyMessages](imapisupport-copymessages.md) , vous devez tout d'abord appeler [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) avec l'indicateur GENERATE_RECEIPT_ONLY défini. La Banque de messages réceptrice n'est pas responsable de la génération de rapports de lecture pour les messages copiés ou déplacés. Si vous appelez **IMAPISupport:: CopyMessages** pour implémenter **IMAPIFolder:: CopyMessages**, n'appelez pas **SetReadFlags**; MAPI l'appelle. 
  
Votre implémentation peut déplacer ou copier les messages dans n'importe quel ordre et générer des rapports d'état de lecture dans n'importe quel ordre. Autrement dit, vous pouvez finir de copier les messages avant de générer les rapports d'état de lecture ou d'envoyer les rapports avant que votre implémentation ne démarre l'opération de copie. Toutefois, les rapports lus doivent être envoyés pour que tous les messages soient copiés, que la copie réussisse ou non.
  
Lorsque l'opération de copie ou de déplacement implique plusieurs messages, effectuez l'opération aussi complètement que possible. N'arrêtez pas l'opération prématurément à moins qu'une défaillance ne se produise au-delà de votre contrôle, telle qu'une mémoire insuffisante, un manque d'espace disque ou une corruption de la Banque de messages.
  
Essayez de maintenir les identificateurs d'entrée entre les opérations de déplacement ou de copie. Vous devez également conserver les identificateurs d'entrée, bien que cela ne soit pas obligatoire.
  
Envoyer des notifications lorsque vous déplacez ou copiez des messages de sorte que les clients soient avertis que leurs appels aux méthodes « [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) » peuvent échouer. 
  
N'incluez pas l'état d'un message dans l'opération de copie ou de déplacement. Le transfert ou la copie d'un état de message affecte grandement les performances.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Utilisez **IMAPIFolder:: CopyMessages** pour remplir les dossiers de résultats de recherche, où les messages sont souvent regroupés par dossier parent. 
  
Attendez-vous à ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**IMAPIFolder:: CopyMessages** a réussi à copier ou déplacer tous les messages.  <br/> |S_OK  <br/> |
|**IMAPIFolder:: CopyMessages** n'a pas pu copier ou déplacer tous les messages.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder:: CopyMessages** n'a pas pu être exécuté.  <br/> |Toute valeur d'erreur  <br/> |
   
Lorsque **IMAPIFolder:: CopyMessages** ne parvient pas à terminer, ne partez pas du principe qu'aucun travail n'a été effectué. **IMAPIFolder:: CopyMessages** peut avoir pu copier ou déplacer un ou plusieurs messages avant de rencontrer l'erreur. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

