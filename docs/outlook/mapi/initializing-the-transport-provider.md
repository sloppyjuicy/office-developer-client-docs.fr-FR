---
title: Initialisation du fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 977c18ce-ece5-4ad1-ac97-5a680846ab83
ms.openlocfilehash: b4d5a12d1e0ef22db36d8e0ab0337d1b6bb06918
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372933"
---
# <a name="initializing-the-transport-provider"></a>Initialisation du fournisseur de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’interface de transport-spooler définit les appels que lepooler MAPI effectue à un fournisseur de transport. Les fournisseurs de transport implémentent ces routines dans une bibliothèque de liens dynamiques (DLL). Le premier point d’entrée direct dans la DLL utilisée par lepooler MAPI doit être la fonction d’initialisation du fournisseur de transport [XPProviderInit](xpproviderinit.md).
  
MAPI utilise la routine **GetProcAddress** pour obtenir l’adresse de la routine d’initialisation du fournisseur de services, puis appelle cette routine. Le nom de la routine d’initialisation est **XPProviderInit** pour les fournisseurs de transport. Il est différent pour les autres types de fournisseurs de services MAPI afin qu’une DLL puisse contenir n’importe quelle combinaison de types de fournisseurs de services, mais un seul fournisseur de services d’un type particulier. Toutefois, un fournisseur de services d’un type donné peut implémenter plusieurs services de ce type. Par exemple, un fournisseur de transport peut implémenter la fonctionnalité de transport de messages à plusieurs services de messagerie. 
  
Le fichier d’en-tête mapispi.h possède une définition de type pour le prototype de fonction de la fonction d’initialisation du fournisseur de transport et un nom de procédure prédéféré pour celui-ci. En nommant les routines d’initialisation dans vos fichiers C et C++ avec les mêmes noms que **getProcAddress** et en utilisant une déclaration d’exportation simple dans votre fichier DLL.DEF, vous obtenez automatiquement la vérification du type des paramètres de votre routine d’initialisation. Consultez l’exemple de code source du fournisseur de transport pour obtenir des exemples. Pour plus d’informations, [voir Exemple de fournisseur de transport](transport-provider-sample.md).
  
Si l’appel d’initialisation d’un fournisseur de services réussit mais renvoie un numéro de version de l’interface de fournisseur de services trop petit pour que MAPI gère, MAPI appelle immédiatement la méthode **Release** de l’objet fournisseur de services et continue comme si l’appel d’initialisation avait échoué avec MAPI_E_VERSION. De cette façon, MAPI et le fournisseur de services définissent conjointement la plage de numéros de version de l’interface du fournisseur de services qu’ils peuvent gérer, et si rien ne correspond, le chargement du fournisseur de services échoue avec une valeur MAPI_E_VERSION de retour. 
  
La dernière étape pour lepooler MAPI lors de l’accès aux ressources du fournisseur de services consiste à se connecter au fournisseur de transport. Lepooler MAPI appelle la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) de l’objet [IXPProvider : IUnknown](ixpprovideriunknown.md) renvoyé par **XPProviderInit**. Il s’agit de l’appel dans lequel les informations d’identification, si elles sont utilisées, sont cochées et les boîtes de dialogue peuvent être autorisées.
  
Si un processus ouvre une deuxième session de transport sur le même fournisseur de transport et la même session MAPI, le fournisseur de transport DLL ne doit pas créer un deuxième objet fournisseur. Le premier objet fournisseur doit être utilisé pour se connecter à la deuxième session de transport. Un fournisseur de transport doit être programmé pour prendre en charge plusieurs sessions de transport dans un seul objet fournisseur. Un deuxième objet fournisseur ne doit être créé que si différentes sessions MAPI sont utilisées dans le même processus.
  

