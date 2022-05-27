---
title: Libération du fournisseur de transport
description: Décrit les étapes lorsque MAPI ou le spouleur MAPI se termine à l’aide d’un objet d’ouverture de session de transport. Cette rubrique s’applique à Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
ms.openlocfilehash: add142ed52aa20aa11bfcdc493b3006278951a49
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752322"
---
# <a name="releasing-the-transport-provider"></a>Libération du fournisseur de transport

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque MAPI ou le spouleur MAPI se termine à l’aide d’un objet d’ouverture de session de transport :
  
1. MAPI ou le spouleur MAPI appelle la méthode [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) du fournisseur de transport. 
    
2. Le fournisseur de transport invalide l’objet d’état en appelant la méthode [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) . Le fait que le fournisseur de transport invalide les objets de message envoyés ou reçus au moment de l’appel **de TransportLogoff** dépend des indicateurs passés à **TransportLogoff**.
    
3. Le fournisseur de transport appelle la méthode [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de l’objet de support pour supprimer la ligne du fournisseur de transport de la table d’état et supprimer des tables internes tous les identificateurs uniques (IUID) qui ont été définis avec la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) . Il décrémente le nombre d’objets d’ouverture de session connus actifs sur cet objet fournisseur. Si le nombre atteint zéro, MAPI appelle la méthode [IXPProvider::Shutdown](ixpprovider-shutdown.md) et **Release** sur l’objet fournisseur. S’il s’agit du dernier objet fournisseur connu utilisant cette DLL sur ce processus, MAPI appelle **ultérieurement la fonction FreeLibrary** sur la DLL. La mémoire de l’objet de support MAPI est libérée et la méthode **Release** de l’objet de support est retournée. 
    
4. La méthode **TransportLogoff** retourne S_OK. 
    
5. MAPI ou le spouleur MAPI appelle **Release** sur l’objet d’ouverture de session du fournisseur de transport. La mémoire de l’objet est libérée. 
    
6. MAPI ou le spouleur MAPI appelle **FreeLibrary** sur la DLL du fournisseur. 
    
Pour des raisons de robustesse, les objets d’ouverture de session et de fournisseur doivent être en mesure de gérer eux-mêmes les appels **de mise en production** finals sans avoir d’abord leurs méthodes **TransportLogoff** ou **Shutdown** appelées. Si **Release** est appelé dans de tels cas, les fournisseurs de transport doivent traiter les appels comme si **TransportLogoff** ou **Shutdown** avait été appelé avec un argument zéro suivi de **Release**.
  

