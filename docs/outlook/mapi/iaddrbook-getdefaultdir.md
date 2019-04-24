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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336693"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie l'identificateur d'entrée pour le conteneur de carnet d'adresses initial.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpcbEntryID_
  
> remarquer Pointeur vers le nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lppEntryID_ . 
    
 _lppEntryID_
  
> remarquer Pointeur vers un pointeur vers l'identificateur d'entrée du conteneur par défaut.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'identificateur d'entrée du conteneur par défaut a été renvoyé.
    
## <a name="remarks"></a>Remarques

Les applications clientes et les fournisseurs de services appellent la méthode **GetDefaultDir** pour récupérer l'identificateur d'entrée du conteneur de carnet d'adresses par défaut. Le conteneur par défaut est ce que l'utilisateur voit affiché dans le carnet d'adresses lors de la première ouverture du carnet d'adresses. Si un conteneur par défaut n'a pas été défini par un appel à la méthode [IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md) , MAPI affecte comme conteneur par défaut le premier conteneur avec des noms qui ne sont pas le carnet d'adresses personnel (PAB). Si un tel conteneur est introuvable, le PAB devient le conteneur par défaut. 
  
Pour définir le répertoire par défaut, un client ou un fournisseur appelle la méthode **SetDefaultDir** . Les clients et les fournisseurs n'ont pas besoin d'appeler la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) ; étant donné que les modifications apportées au carnet d'adresses ne sont pas traitées, les modifications sont immédiatement rendues permanentes. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnOpenDefaultDir  <br/> |MFCMAPI utilise la méthode **GetDefaultDir** pour obtenir l'ID du conteneur de carnet d'adresses par défaut.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

