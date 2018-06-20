---
title: Automatisation d’InfoPath à partir d’une application externe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath fournit automation d’application à partir du code écrit à l’aide de COM et script à l’aide des méthodes de l’objet Application et de la collection XDocuments.
ms.openlocfilehash: 0e3fcc50ec11f5fc8791d37144767bf0398ccda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782249"
---
# <a name="automating-infopath-from-an-external-application"></a>Automatisation d’InfoPath à partir d’une application externe

Microsoft InfoPath fournit automation d’application à partir du code écrit à l’aide de COM et script à l’aide des méthodes de l’objet **Application** et de la collection **XDocuments** . 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Vue d’ensemble de l’Application et les objets XDocument

L’objet **Application** contient les méthodes suivantes utilisées pour l’automation : 
  
|**Méthode**|**Description**|
|:-----|:-----|
|**CacheSolution** <br/> |Examine le dans le cache et, si nécessaire, met à jour à partir de l’emplacement publié du modèle de formulaire.  <br/> |
|**Quit** <br/> |Quitte l’application Microsoft Office InfoPath.  <br/> |
|**RegisterSolution** <br/> |Installe le modèle de formulaire Microsoft Office InfoPath spécifié.  <br/> |
|**UnregisterSolution** <br/> |Désinstalle le modèle de formulaire Microsoft Office InfoPath spécifié.  <br/> |
   
La collection **XDocuments** contient les méthodes suivantes qui peuvent être utilisés pour l’automatisation externe : 
  
|**Méthode**|**Description**|
|:-----|:-----|
|Méthode **Close**  <br/> |Ferme le formulaire Microsoft Office InfoPath spécifié.  <br/> |
|Méthode **New**  <br/> |Crée un nouveau formulaire Microsoft Office InfoPath.  <br/> |
|Méthode **NewFromSolution**  <br/> |Crée un nouveau formulaire Microsoft Office InfoPath basé sur le modèle de formulaire spécifié.  <br/> |
|Méthode **NewFromSolutionWithData**  <br/> |Crée un nouveau formulaire Microsoft Office InfoPath utilisant le modèle de formulaire et les données XML spécifié.  <br/> |
|Méthode **Open**  <br/> |Ouvre le formulaire Microsoft Office InfoPath spécifié.  <br/> |
   
Pour utiliser l’objet **Application** d’une application externe, vous utilisez la fonction **CreateObject** avec le ProgID de l’application InfoPath (« InfoPath.Application ») pour créer une variable objet qui représente l’application InfoPath. Vous pouvez ensuite utiliser la propriété **XDocuments** pour accéder à la collection **XDocuments** et ses méthodes pour ouvrir ou créer un formulaire InfoPath. L’exemple suivant illustre la création d’une référence à l’objet **d’Application** à l’aide de Microsoft Visual Basic 6.0 ou Visual Basic pour Applications (VBA) langage de programmation : 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Étant donné que la fonction **CreateObject** crée une variable d’objet à l’aide de la liaison tardive, la saisie semi-automatique ne sera pas disponible dans Visual Basic Editor. Consultez les liens dans les tableaux ci-dessus pour plus d’informations sur la syntaxe d’appel correcte. 
  

