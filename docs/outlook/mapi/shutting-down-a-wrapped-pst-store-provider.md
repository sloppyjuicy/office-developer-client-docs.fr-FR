---
title: Arrêt d’un fournisseur de magasin PST encapsulé
description: Décrit comment arrêter correctement le fournisseur de magasin PST encapsulé une fois que vous avez terminé d’utiliser un fournisseur de magasin PST encapsulé.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
ms.openlocfilehash: 507c01e5306b2d4e55ca87919bc9b529f739722c
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894200"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Arrêt d’un fournisseur de magasin PST encapsulé

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une fois que vous avez terminé d’utiliser un fournisseur de magasins de fichiers PST (Personal Folders) encapsulé, vous devez arrêter correctement le fournisseur du magasin PST encapsulé. Pour plus d’informations sur l’utilisation du fournisseur de magasin PST encapsulé, consultez [Utilisation d’un fournisseur de magasin PST encapsulé](using-a-wrapped-pst-store-provider.md).
  
Pour arrêter un fournisseur de magasin PST encapsulé, vous devez appeler la fonction **[IMSProvider::Shutdown](imsprovider-shutdown.md)** . Cette fonction ferme le fournisseur du magasin PST encapsulé de manière ordonnée. 
  
Dans cette rubrique, la fonction **IMSProvider::Shutdown** est illustrée à l’aide d’un exemple de code de l’exemple de fournisseur de magasin PST encapsulé. L’exemple implémente un fournisseur PST encapsulé qui est destiné à être utilisé conjointement avec l’API de réplication. Pour plus d’informations sur le téléchargement et l’installation de l’exemple de fournisseur de magasin PST encapsulé, consultez [l’installation de l’exemple de fournisseur de magasin PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d’informations sur l’API de réplication, consultez [À propos de l’API de réplication](about-the-replication-api.md).
  
## <a name="shut-down-routine"></a>Arrêter la routine

Le spouleur MAPI appelle la fonction **[IMSProvider::Shutdown](imsprovider-shutdown.md)** juste avant de libérer le fournisseur de magasin PST encapsulé afin que le fournisseur de magasin PST encapsulé puisse s’arrêter correctement. La fonction met fin à tous les objets de session associés au fournisseur de magasin PST encapsulé. 
  
## <a name="cmsprovidershutdown-example"></a>EXEMPLE CMSProvider::ShutDown()

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



[À propos de l’exemple de fournisseur de magasin PST encapsulé](about-the-sample-wrapped-pst-store-provider.md)
  
[Installation de l’exemple de fournisseur de magasin PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md)
  
[Initialisation d’un fournisseur de magasin PST encapsulé](initializing-a-wrapped-pst-store-provider.md)
  
[Connexion à un fournisseur de magasin PST encapsulé](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Utilisation d’un fournisseur de magasin PST encapsulé](using-a-wrapped-pst-store-provider.md)

