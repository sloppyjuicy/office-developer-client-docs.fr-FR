---
title: Démarrage d’une session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d88ce382b6a6b5f98ec5f88c4deb1565d3b60151
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382588"
---
# <a name="starting-a-mapi-session"></a>Démarrage d’une session MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Bien qu’il existe une quantité importante de travail effectué au cours de la session de démarrage, les tâches requises sont minimes. Cette opération est effectuée dans l’interface MAPI de traitement des appels [exécuter MAPIInitialize](mapiinitialize.md) et [MAPILogonEx](mapilogonex.md) . Ces deux fonctions acceptent des indicateurs en tant que paramètres d’entrée pour contrôler des aspects de la session de gestion de la notification et l’interface utilisateur. Il est important de comprendre les conséquences de la définition de chacune de ces indicateurs lors de l’appel **exécuter MAPIInitialize** pour initialiser les bibliothèques MAPI et **MAPILogonEx** pour ouvrir une session sur le sous-système MAPI. 
  
 **Pour démarrer une session MAPI**
  
1. Appelez **exécuter MAPIInitialize** pour initialiser l’ensemble standard de bibliothèques de MAPI. 
    
2. Si vous devez utiliser les bibliothèques OLE, appelez la fonction OLE [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).
    
3. Si vous devez utiliser la bibliothèque d’utilitaires MAPI, appelez [ScInitMapiUtil](scinitmapiutil.md).
    
4. Appelle **MAPILogonEx** avec un profil valide pour ouvrir une session sur le sous-système MAPI. **MAPILogonEx** vérifie la configuration de chacun des fournisseurs de services dans les services de message inclus dans le profil, inviter l’utilisateur pour plus d’informations si nécessaire et possible. Lorsque **MAPILogonEx** est terminée, les fournisseurs de service configuré sont prêts pour le service. 
    
## <a name="in-this-section"></a>Dans cette section

[Initialisation de MAPI](initializing-mapi.md)
  
> Décrit comment initialiser MAPI pour une session.
    
[Initialisation d’OLE pour MAPI](initializing-ole-for-mapi.md)
  
> Décrit les appels s’initialiser OLE pour une utilisation avec MAPI.
    
[Initialisation des utilitaires MAPI](initializing-the-mapi-utilities.md)
  
> Décrit comment initialiser les utilitaires MAPI.
    
[Connexion à MAPI](logging-on-to-mapi.md)
  
> Décrit comment les applications clientes se connecter au système sub MAPI.
    

