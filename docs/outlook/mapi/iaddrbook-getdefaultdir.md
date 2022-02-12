---
title: IAddrBookGetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1b6fab981d2ae40b60ab6414083ad42fb8a400c0
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784250"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie l’identificateur d’entrée pour le conteneur de carnet d’adresses initial.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’byte dans l’identificateur d’entrée pointé par  _le paramètre lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée du conteneur par défaut.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’identificateur d’entrée du conteneur par défaut a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

Les applications clientes et les fournisseurs de services appellent la méthode **GetDefaultDir** pour récupérer l’identificateur d’entrée du conteneur de carnet d’adresses par défaut. Le conteneur par défaut est ce que l’utilisateur voit s’afficher dans le carnet d’adresses lors de la première ouverture du carnet d’adresses. Si un conteneur par défaut n’a pas été définie par un appel à la méthode [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) , MAPI affecte comme conteneur par défaut le premier conteneur avec des noms qui ne sont pas le carnet d’adresses personnel( PAB). Si un tel conteneur est in trouver, le PAB devient le conteneur par défaut. 
  
Pour définir le répertoire par défaut, un client ou un fournisseur appelle la **méthode SetDefaultDir** . Les clients et fournisseurs n’ont pas besoin d’appeler la [méthode IMAPIProp::SaveChanges](imapiprop-savechanges.md) ; étant donné que les modifications apportées au carnet d’adresses ne sont pas prises en compte, les modifications sont immédiatement rendues permanentes. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenDefaultDir  <br/> |MFCMAPI utilise la **méthode GetDefaultDir** pour obtenir l’ID du conteneur de carnet d’adresses par défaut. |
   
## <a name="see-also"></a>Voir aussi



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

