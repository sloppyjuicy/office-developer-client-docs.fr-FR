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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e6e9e9cefc75ffc78ee7beb47e89063ea1a66ce7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783722"
---
# <a name="imapifoldercopymessages"></a>IMAPIFolder::CopyMessages

  
  
**S’applique à**: Outlook 
  
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
  
> [in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui identifient l’ou les messages pour copier ou déplacer. 
    
 _lpInterface_
  
> [in] Un pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier de destination indiqué par le paramètre _lpDestFolder_ . Passant NULL entraîne le renvoi de l’interface de dossier standard, du fournisseur de services [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Les clients doivent passer la valeur NULL. Autres appelants peuvent de définir le paramètre _lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Pointeur vers le dossier ouvert pour recevoir les messages copiés ou déplacées.
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent des boîtes de dialogue ni windows cette méthode affiche. Le paramètre _ulUIParam_ est ignoré à moins que le client définit l’indicateur MESSAGE_DIALOG dans le paramètre _ulFlags_ et transmet la valeur NULL dans le paramètre _lpProgress_ . 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la manière dont l’opération de copie ou de déplacement est effectuée. Les indicateurs suivants peuvent être définis :
    
MAPI_DECLINE_OK 
  
> Informe le fournisseur de banque de messages pour retourner immédiatement MAPI_E_DECLINE_COPY si elle implémente **IMAPIFolder::CopyMessages** en appelant la méthode [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) de l’objet de la prise en charge. 
    
MESSAGE_DIALOG 
  
> Affiche un indicateur de progression de l’opération.
    
MESSAGE_MOVE 
  
> L’ou les messages doivent être déplacés et non copiés. Si MESSAGE_MOVE n’est pas définie, les messages sont copiés.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’ou les messages ont été correctement copiés ou déplacés.
    
MAPI_E_DECLINE_COPY 
  
> Le fournisseur implémente cette méthode en appelant une méthode de prise en charge de l’objet et l’appelant a passé l’indicateur MAPI_DECLINE_OK.
    
MAPI_W_PARTIAL_COMPLETION SE PRODUIT 
  
> L’appel a réussi, mais pas toutes les entrées ont été correctement copiées ou déplacées. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::CopyMessages** copie ou déplace les messages vers un autre dossier. 
  
Les messages qui sont ouvertes avec en lecture/écriture autorisation peut être déplacée ou copiée. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Si vous copiez les messages vers une autre banque de messages sans utiliser la méthode [IMAPISupport::CopyMessages](imapisupport-copymessages.md) , vous devez d’abord appeler [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) avec l’indicateur GENERATE_RECEIPT_ONLY. La banque de message de réception n’est pas responsable de la génération de rapports de lecture pour les messages copiés ou déplacées. Si vous appelez **IMAPISupport::CopyMessages** pour mettre en œuvre **IMAPIFolder::CopyMessages**, n’appelez pas **SetReadFlags**; MAPI est l’appeler. 
  
Votre implémentation peut déplacer ou copier les messages dans n’importe quel ordre et générer des rapports d’état de lecture dans n’importe quel ordre. Autrement dit, vous pouvez terminer la copie des messages avant de générer des rapports d’état de lecture ou envoyer les rapports avant que votre implémentation démarre l’opération de copie. Toutefois, lire les rapports doivent être envoyés pour tous les messages à copier, indépendamment de si la copie a réussi.
  
Lorsque l’opération de copie ou de déplacement implique plusieurs messages, effectuez l’opération complètement que possible. N’arrêtez pas l’opération prématurément, sauf si une panne se produit qui est votre volonté, telles que le manque de mémoire, manque d’espace disque ou l’endommagement de la banque de messages.
  
Essayez de mettre à jour les identificateurs d’entrée pour les opérations de déplacement ou de copie. Vous devez également conserver les identificateurs d’entrée, bien qu’il ne soit pas requis.
  
Envoyer des notifications lorsque vous déplacez ou copiez des messages afin que les clients sont avertis que leurs appels aux méthodes de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) des messages peuvent échouer. 
  
Ne pas inclure l’état d’un message dans la copie ou l’opération de déplacement. Déplacement ou copie d’un état de message considérablement affecte les performances.
  
## <a name="notes-to-callers"></a>Notes aux appelants

**IMAPIFolder::CopyMessages** permet de remplir les dossiers des résultats de recherche, dans laquelle les messages sont souvent regroupés par dossier parent. 
  
Prévoyez ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages** a été copié ou déplacé chaque message.  <br/> |S_OK  <br/> |
|**IMAPIFolder::CopyMessages** n’a pas pu copier ou déplacer tous les messages.  <br/> |MAPI_W_PARTIAL_COMPLETION SE PRODUIT  <br/> |
|**IMAPIFolder::CopyMessages** n’a pas pu terminer.  <br/> |Une valeur d’erreur  <br/> |
   
Lorsque **IMAPIFolder::CopyMessages** est impossible de terminer, ne supposent qu’aucun travail n’a été effectuée. **IMAPIFolder::CopyMessages** a pu copier ou déplacer un ou plusieurs messages avant de rencontrer l’erreur. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

