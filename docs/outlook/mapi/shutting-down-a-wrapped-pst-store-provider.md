---
title: Arrêt d'un fournisseur de magasins PST encapsulé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Dernière modification le: 02 juillet 2012'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409943"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Arrêt d'un fournisseur de magasins PST encapsulé

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une fois que vous avez fini d'utiliser un fournisseur de magasins de fichiers de dossiers personnels (PST), vous devez arrêter correctement le fournisseur de magasins PST encapsulé. Pour plus d'informations sur l'utilisation du fournisseur de magasins PST encapsulé, consultez la rubrique [using a wrappedd PST Store Provider](using-a-wrapped-pst-store-provider.md).
  
Pour arrêter un fournisseur de magasins PST encapsulé, vous devez appeler la fonction **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** . Cette fonction ferme le fournisseur de magasins PST encapsulé de manière ordonnée. 
  
Dans cette rubrique, la fonction **IMSProvider:: Shutdown** est illustrée à l'aide d'un exemple de code à partir de l'exemple de fournisseur de magasins PST encapsulé. L'exemple implémente un fournisseur PST encapsulé destiné à être utilisé conjointement avec l'API de réPlication. Pour plus d'informations sur le téléchargement et l'installation de l'exemple de fournisseur de magasins PST encapsulé, consultez [la rubrique installation de l'exemple de fournisseur de magasins PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d'informations sur l'API de réPlication, voir [à propos de l'API](about-the-replication-api.md)de réplication.
  
## <a name="shut-down-routine"></a>Arrêter la routine

Le spouleur MAPI appelle la fonction **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** juste avant de libérer le fournisseur de magasins PST encapsulé afin que le fournisseur de magasins PST encapsulé puisse s'arrêter correctement. La fonction met fin à tous les objets session associés au fournisseur de magasins PST encapsulé. 
  
## <a name="cmsprovidershutdown-example"></a>CMSProvider:: ShutDown () exemple

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



[À propos de l'exemple de fournisseur de banque d'informations PST encapsulé](about-the-sample-wrapped-pst-store-provider.md)
  
[Installation de l'exemple de fournisseur de magasins PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md)
  
[Initialisation d'un fournisseur de magasins PST encapsulé](initializing-a-wrapped-pst-store-provider.md)
  
[Connexion à un fournisseur de magasins PST encapsulé](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Utilisation d'un fournisseur de magasins PST encapsulé](using-a-wrapped-pst-store-provider.md)

