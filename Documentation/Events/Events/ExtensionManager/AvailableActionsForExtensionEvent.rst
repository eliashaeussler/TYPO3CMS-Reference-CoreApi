.. include:: /Includes.rst.txt
.. index:: Events; AvailableActionsForExtensionEvent
.. _AvailableActionsForExtensionEvent:


=================================
AvailableActionsForExtensionEvent
=================================

.. versionadded:: 10.3

Event that is triggered when rendering an additional action (currently within
a Fluid ViewHelper) in the Extension Manager.

.. code-block:: php
   :caption: EXT:some_extension/Classes/EventListener/MyEventListener.php


   public function getActions(): array
   {
       return $this->actions;
   }

   public function addAction(string $actionKey, string $content): void
   {
       $this->actions[$actionKey] = $content;
   }

   public function setActions(array $actions): void
   {
       $this->actions = $actions;
   }


API
---

.. include:: /CodeSnippets/Events/ExtensionManager/AvailableActionsForExtensionEvent.rst.txt
