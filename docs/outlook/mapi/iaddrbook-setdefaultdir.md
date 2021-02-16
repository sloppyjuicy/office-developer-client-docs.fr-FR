---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3ab01f189734ac30b4c027f4e5596c88031b5f99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341698"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Établit le conteneur spécifié en tant que conteneur de carnet d’adresses par défaut.
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du conteneur de carnet d’adresses par défaut.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le conteneur de carnet d’adresses par défaut a été correctement définie.
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de services appellent la **méthode SetDefaultDir** pour établir un nouveau conteneur de carnet d’adresses par défaut. Le conteneur par défaut est celui que l’utilisateur voit s’afficher dans le carnet d’adresses lors de sa première ouverture. **SetDefaultDir enregistre** le conteneur par défaut en tant qu’entrée dans le profil. Le conteneur reste le conteneur par défaut jusqu’à ce qu’un autre appel à **SetDefaultDir** soit effectué dans la même session ou dans une autre session, ou que le conteneur soit supprimé. 
  
> [!NOTE]
> La [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) correspond au paramètre **Choisir** automatiquement dans la boîte de dialogue Options du carnet d’adresses. Lorsque cette propriété existe dans la section profil [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) et est définie sur **true**, la boîte de dialogue carnet d’adresses n’est plus définie par défaut sur le conteneur spécifié par **SetDefaultDir**, mais choisit un carnet d’adresses que Microsoft Outlook considère approprié pour le contexte dans lequel la boîte de dialogue a été affichée. Notez que cela peut entraîner une expérience médiocre pour les fournisseurs de carnets d’adresses tiers. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|Abcontdlg.cpp  <br/> |CAbContDlg::OnSetDefaultDir  <br/> |MFCMAPI utilise la **méthode SetDefaultDir** pour définir le conteneur de carnet d’adresses spécifié comme conteneur par défaut.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

