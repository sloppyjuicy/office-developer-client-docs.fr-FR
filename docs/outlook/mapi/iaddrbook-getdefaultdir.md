---
title: IAddrBookGetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a9f0fac76f06bd638aeff89ff096507209cc0287
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568454"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie l’identificateur d’entrée pour le conteneur de carnet d’adresses initiale.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée du conteneur par défaut.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’identificateur d’entrée du conteneur par défaut a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

Fournisseurs de services et applications clientes appellent la méthode **GetDefaultDir** pour récupérer l’identificateur d’entrée du conteneur de carnet d’adresses par défaut. Le conteneur par défaut est ce que l’utilisateur voit affiché dans le carnet d’adresses lors de la première ouverture du carnet d’adresses. Si un conteneur par défaut n’a pas été défini par un appel à la méthode [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) , MAPI affecte en tant que le conteneur par défaut le premier conteneur avec des noms qui n’est pas le carnet d’adresses personnel (CAP). Si le conteneur est introuvable, le carnet d’adresses personnel devient le conteneur par défaut. 
  
Pour définir la valeur par défaut directory, un client ou un fournisseur appelle la méthode **SetDefaultDir** . Clients et fournisseurs n’ont pas d’appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ; Étant donné que les modifications apportées au carnet d’adresses ne sont pas traitées, les modifications sont apportées immédiatement définitive. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenDefaultDir  <br/> |MFCMAPI utilise la méthode **GetDefaultDir** pour obtenir l’ID pour le conteneur de carnet d’adresses par défaut.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

