---
title: Arrêt d’un fournisseur de magasin PST wrapped
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 3f4aa55a8b557c8c14678bea618b761a22d7f96a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619756"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Arrêt d’un fournisseur de magasin PST wrapped

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une fois que vous avez terminé d’utiliser un fournisseur de magasin de dossiers personnels (PST) wrapped, vous devez arrêter correctement le fournisseur de magasin PST wrapped. Pour plus d’informations sur l’utilisation du fournisseur de magasin PST [wrapped, voir Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).
  
Pour arrêter un fournisseur de magasin PST wrapped, vous devez appeler la **[fonction IMSProvider::Shutdown.](imsprovider-shutdown.md)** Cette fonction ferme le fournisseur de magasin PST wrapped de manière ordonnée. 
  
Dans cette rubrique, la fonction **IMSProvider::Shutdown** est démontrée à l’aide d’un exemple de code du fournisseur de magasin PST Wrapped sample. L’exemple implémente un fournisseur PST wrapped qui est destiné à être utilisé conjointement avec l’API de réplication. Pour plus d’informations sur le téléchargement et l’installation de l’exemple de fournisseur de magasin PST [Wrapped, voir Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d’informations sur l’API de réplication, voir [à propos de l’API de réplication.](about-the-replication-api.md)
  
## <a name="shut-down-routine"></a>Shut Down Routine

Lepooler MAPI appelle la fonction **[IMSProvider::Shutdown](imsprovider-shutdown.md)** juste avant de libérer le fournisseur de magasin PST wrapped afin que le fournisseur de magasin PST wrapped puisse s’arrêter correctement. La fonction met fin à tous les objets de session associés au fournisseur de magasin PST wrapped. 
  
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



[À propos de l’exemple de fournisseur de magasins PST wrapped](about-the-sample-wrapped-pst-store-provider.md)
  
[Installation de l’exemple de fournisseur de magasin PST Wrapped](installing-the-sample-wrapped-pst-store-provider.md)
  
[Initialisation d’un fournisseur de magasin PST wrapped](initializing-a-wrapped-pst-store-provider.md)
  
[Connexion à un fournisseur de magasin PST wrapped](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Utilisation d’un fournisseur de magasin PST wrapped](using-a-wrapped-pst-store-provider.md)

