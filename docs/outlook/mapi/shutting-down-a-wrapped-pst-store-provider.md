---
title: Arrêt d’un fournisseur d’archive PST encapsulée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Dernière modification : 02 juillet 2012'
ms.openlocfilehash: 43a65548bedc1729ff2bcb62bc3df78d2408bf12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571744"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Arrêt d’un fournisseur d’archive PST encapsulée

 
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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



[À propos de l’exemple de fournisseur d’archive PST encapsulée](about-the-sample-wrapped-pst-store-provider.md)
  
[Installation de l’exemple de fournisseur d’archive PST encapsulée](installing-the-sample-wrapped-pst-store-provider.md)
  
[Initialisation d’un fournisseur d’archive PST encapsulée](initializing-a-wrapped-pst-store-provider.md)
  
[Connexion à un fournisseur d’archive PST encapsulée](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Utilisation d’un fournisseur d’archive PST encapsulée](using-a-wrapped-pst-store-provider.md)

