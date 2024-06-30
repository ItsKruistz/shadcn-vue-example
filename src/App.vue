<script setup lang="ts">
import { Button } from '@/components/ui/button'

import {
  Accordion,
  AccordionContent,
  AccordionItem,
  AccordionTrigger,
} from '@/components/ui/accordion'

import {
  Dialog,
  DialogContent,
  DialogDescription,
  DialogFooter,
  DialogHeader,
  DialogTitle,
  DialogTrigger,
} from '@/components/ui/dialog'

import {
  Cloud,
  CreditCard,
  Github,
  Keyboard,
  LifeBuoy,
  LogOut,
  Mail,
  MessageSquare,
  Plus,
  PlusCircle,
  Settings,
  User,
  UserPlus,
  Users,
} from 'lucide-vue-next'

import {
  DropdownMenu,
  DropdownMenuContent,
  DropdownMenuGroup,
  DropdownMenuItem,
  DropdownMenuLabel,
  DropdownMenuPortal,
  DropdownMenuSeparator,
  DropdownMenuShortcut,
  DropdownMenuSub,
  DropdownMenuSubContent,
  DropdownMenuSubTrigger,
  DropdownMenuTrigger,
} from '@/components/ui/dropdown-menu'

import { DialogClose } from 'radix-vue'

import {
  Select,
  SelectContent,
  SelectGroup,
  SelectItem,
  SelectLabel,
  SelectTrigger,
  SelectValue,
} from '@/components/ui/select'

import { Tabs, TabsContent, TabsList, TabsTrigger } from '@/components/ui/tabs'

import {
  Tooltip,
  TooltipContent,
  TooltipProvider,
  TooltipTrigger,
} from '@/components/ui/tooltip'

const defaultValue = 'item-3'
const accordionItems = [
  {
    value: 'item-1',
    title: 'Is it accessible?',
    content: 'Yes. It adheres to the WAI-ARIA design pattern.',
  },
  {
    value: 'item-2',
    title: 'Is it unstyled?',
    content:
      "Yes. It's unstyled by default, giving you freedom over the look and feel.",
  },
  {
    value: 'item-3',
    title: 'Can it be animated?',
    content: 'Yes! You can use the transition prop to configure the animation.',
  },
]

function toggleDarkMode() {
  const root = document.querySelector(':root')
  root?.classList.toggle('dark')
}

function changeTheme(theme: string): void {
  let root = document.querySelector(':root')

  const isDark = root?.classList.contains('dark')

  root.className = ''
  if (isDark) root?.classList.add('dark')
  root?.classList.add(theme)
}
</script>

<template>
  <div>
  <section class="body-font">
  <div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
    <div class="lg:flex-grow md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-left text-left">
      <h1 class="title-font text-4xl mb-4 font-figtree font-bold">Hello, I'm Kruistz!</h1>
      <p class="mb-8 leading-normal font-figtree text-lg">An hobbyist coder  who likes to play gacha games. I  also like to take photos too!</p>
    </div>
    <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6">
      <img class="object-cover object-center rounded" alt="hero" src="https://dummyimage.com/720x600">
    </div>
  </div>
</section>
  </div>
</template>
