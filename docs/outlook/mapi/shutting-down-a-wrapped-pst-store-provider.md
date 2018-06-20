---
title: Arrêt d’un fournisseur de banque de dossiers personnels encapsulé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Dernière modification : 02 juillet 2012'
ms.openlocfilehash: 5c8ad7443b0c1aa05f48284e4b09859ab53dd2c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787156"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Arrêt d’un fournisseur de banque de dossiers personnels encapsulé

 
  
**S’applique à**: Outlook 
  
Après avoir utilisant un fournisseur de magasin de dossiers personnels (PST) de fichier encapsulé, vous devez fermer correctement le fournisseur de banque PST justifié. Pour plus d’informations sur l’utilisation du fournisseur de magasin PST encapsulé, voir [utilisation d’un fournisseur de magasin encapsulé PST](using-a-wrapped-pst-store-provider.md).
  
Pour arrêter un fournisseur de magasins PST encapsulé, vous devez appeler la fonction **[IMSProvider::Shutdown](imsprovider-shutdown.md)** . Ces fonctions ferme le fournisseur de banque PST justifié de manière ordonnée. 
  
Dans cette rubrique, la fonction **IMSProvider::Shutdown** est illustrée à l’aide d’un exemple de code à partir du fournisseur de magasin exemple encapsulé PST. L’exemple implémente un fournisseur PST renvoyé à la ligne qui est destiné à être utilisé conjointement avec l’API de réplication. Pour plus d’informations sur le téléchargement et l’installation du fournisseur de magasin exemple encapsulé PST, voir [installer le fournisseur de banque exemple encapsulé PST](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d’informations sur l’API de réplication, consultez la rubrique [Sur l’API de réplication](about-the-replication-api.md).
  
## <a name="shut-down-routine"></a>Arrêter de Routine

Le spouleur MAPI appelle la fonction **[IMSProvider::Shutdown](imsprovider-shutdown.md)** juste avant qu’il libère le fournisseur de banque PST encapsulé afin que le fournisseur de banque PST encapsulé peut s’arrêter. La fonction s’arrête tous les objets de session associés au fournisseur de magasin PST justifié. 
  
## <a name="cmsprovidershutdown-example"></a>Exemple CMSProvider::ShutDown()

```cpp
STDMETHODIMP CMSProvider::Shutdown(ULONG * pulFlags) 
{ 
    HRESULT hRes = S_OK; 
    Log(true,"CMSProvider::Shutdown\n"); 
    hRes =m_pPSTMS->Shutdown(pulFlags); 
    Log(true,"CMSProvider::Shutdown returned: 0x%08X\n", hRes); 
    return hRes ;  
}
```

## <a name="see-also"></a>Voir aussi



[À propos de l’exemple de wrapper fournisseur de banque de dossiers personnels](about-the-sample-wrapped-pst-store-provider.md)
  
[Installation de l’exemple de wrapper fournisseur de banque de dossiers personnels](installing-the-sample-wrapped-pst-store-provider.md)
  
[L’initialisation d’un fournisseur de banque de dossiers personnels encapsulé](initializing-a-wrapped-pst-store-provider.md)
  
[Se connecter à un fournisseur de banque de dossiers personnels encapsulé](logging-on-to-a-wrapped-pst-store-provider.md)
  
[À l’aide d’un fournisseur de banque de dossiers personnels encapsulé](using-a-wrapped-pst-store-provider.md)

