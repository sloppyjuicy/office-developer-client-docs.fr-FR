---
title: À l’aide d’un fournisseur de magasins PST encapsulé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Dernière modification : 03 juillet 2012'
ms.openlocfilehash: 4a2ccbbcdd3459af6b69156d80b37695251ba8d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787440"
---
# <a name="using-a-wrapped-pst-store-provider"></a>À l’aide d’un fournisseur de magasins PST encapsulé

**S’applique à**: Outlook 
  
Avant de pouvoir utiliser un fournisseur de magasins encapsulé dossiers personnels (PST) de fichier, vous devez initialiser et configurer le fournisseur de banque PST justifié. Une fois que le fournisseur de banque PST encapsulé est configuré, vous devez implémenter les fonctions afin que MAPI et le spouleur MAPI peuvent se connecter au fournisseur de magasin de message. Pour plus d’informations sur l’initialisation et de se connecter à un fournisseur de magasin PST encapsulé, voir [l’initialisation d’un fournisseur de magasin encapsulé PST](initializing-a-wrapped-pst-store-provider.md) et [l’enregistrement à un fournisseur de magasin encapsulé PST](logging-on-to-a-wrapped-pst-store-provider.md).
  
L’interface **[IMAPISupport::IUnknown](imapisupportiunknown.md)** fournit des implémentations des tâches fréquemment effectuées par message stockent des fournisseurs. Cette interface doit être entourée du exemple encapsulé PST magasin fournisseur à utiliser. La fonction **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** requiert l’implémentation spéciale. Toutes les autres fonctions peuvent passer leurs paramètres à l’objet sous-jacent encapsulé. 
  
Dans cette rubrique, la fonction **IMAPISupport::OpenProfileSection** est illustrée à l’aide d’un exemple de code à partir du fournisseur de magasin exemple encapsulé PST. L’exemple implémente un fournisseur PST renvoyé à la ligne qui est destiné à être utilisé conjointement avec l’API de réplication. Pour plus d’informations sur le téléchargement et l’installation du fournisseur de magasin exemple encapsulé PST, voir [installer le fournisseur de banque exemple encapsulé PST](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d’informations sur l’API de réplication, consultez la rubrique [Sur l’API de réplication](about-the-replication-api.md).
  
Lorsque vous avez terminé à l’aide d’un fournisseur de magasins PST encapsulé, vous devez fermer correctement le fournisseur de banque PST justifié. Pour plus d’informations, voir [Arrêt un fournisseur de magasin PST encapsulé](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Routine Open Section de profil

La fonction **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** ouvre une section du profil actuel. La fonction nécessite un traitement spécial dans l’implémentation du fournisseur de magasin PST justifié. Lors de la `pgNSTGlobalProfileSectionGuid` est demandé, la fonction renvoie la section profil qui est mis en cache. 
  
### <a name="csupportopenprofilesection-example"></a>Exemple CSupport::OpenProfileSection()

```cpp
STDMETHODIMP CSupport::OpenProfileSection( 
    LPMAPIUID lpUid,     
    ULONG ulFlags, 
    LPPROFSECT * lppProfileObj) 
{ 
    Log(true,"CSupport::OpenProfileSection\n"); 
    if (lpUid &&  
        IsEqualMAPIUID(lpUid, (void *)&pbNSTGlobalProfileSectionGuid) &&  
        m_lpProfSect) 
    {      
        // Allow the opening of the Global Section 
        if (m_lpProfSect) 
        { 
            *lppProfileObj = m_lpProfSect; 
            (*lppProfileObj)->AddRef(); 
            return S_OK; 
        } 
    } 
    return m_pMAPISup->OpenProfileSection(lpUid, ulFlags, lppProfileObj); 
}
```

## <a name="see-also"></a>Voir aussi

- [À propos de l’exemple de wrapper fournisseur de banque de dossiers personnels](about-the-sample-wrapped-pst-store-provider.md)
- [Installation de l’exemple de wrapper fournisseur de banque de dossiers personnels](installing-the-sample-wrapped-pst-store-provider.md)
- [L’initialisation d’un fournisseur de banque de dossiers personnels encapsulé](initializing-a-wrapped-pst-store-provider.md)
- [Se connecter à un fournisseur de banque de dossiers personnels encapsulé](logging-on-to-a-wrapped-pst-store-provider.md)
- [Arrêt d’un fournisseur de banque de dossiers personnels encapsulé](shutting-down-a-wrapped-pst-store-provider.md)

